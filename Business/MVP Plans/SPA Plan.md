SPA requirements
Version: 0.3
Primary goal
Convert AppSheet app into web app
Basic ticketing system with status, workflow, users, database, API calls
0. Technology stack
Server: Azure App Services then Azure Ubuntu VM
Framework: Django (MVT pattern)
Front-end: Next.js
Database: PostgreSQL 
CI/CD: GitHub
Version Control: Git
Testing: TBD
Performance Monitoring: Azure Monitor
Security: HTTPS + TBD
Authentication: OAuth
Backup and Disaster Recovery: Azure Backup, Azure Site Recovery
1. **User Login**
   - Necessity of username (email) and password fields only.
Table User maintains users with 
User	
Role	
Maintenance approver	
Purchasing approver	
Global approver	
Cataloger	
Maximo admin
Site	
Language
Status
   - Requirement of additional authentication methods.
- SSO with Google/Microsoft account, ideally native in technology stack
- (future) SSO with social accounts, native in technology stack

   - Integration with social media logins.

2. **Forget/Reset Password**
   - Importance of password reset functionality.
- ideally native in technology stack
   - Procedure for initiating password reset.
- When no SSO, send link to user email to reset password, ideally native in technology stack
   - Specific security considerations.
- Ease of integration of MFA functionality later on

3. **User Registration**
   - Requirement of user registration for the web app.
- Ideally can be requested from app, native in technology stack adding a row for the email address of the requester in user table in status REQUESTED
- Then app admin or global approver activate the user by updating the status of the user from REQUESTED to ACTIVE
- The user rights to the app can be declined by changing the user status to REJECTED
- The user rights to the app can be removed by changing the user status to INACTIVE
   - Necessary fields for registration.
	- See above
   - Specifics on user data collection and registration process.
	- GDPR
   - Email verification for registration.
	- Ideally native in technology stack

4. **User Roles**
   - Available user roles within the system. 
App admin
Requester
Approver (maintenance)
Approver (purchasing)
Cataloger
Approver (global)
CMMS administrator

   - Responsibilities assigned to each user role.

Each role comes with
Default view
Authorized request status transition
Restricted actions, views, field, and rows
…


Role
View permission
Rows
Default view
Requester
My requests
All requests per row security
My requests
Approver (maintenance)
My approval requests
All requests per row security, with status Awaiting maintenance approval
My approval requests
Approver (purchasing)
My approval requests
All requests per row security, with status Awaiting purchasing approval
My approval requests
Cataloger
My cataloging requests, All requests
All requests per row security, with status Awaiting cataloging
My cataloging requests
Approver (global)
My approval requests, All requests
All requests per row security, with status Awaiting global approval
All requests per 
My approval requests
CMMS administrator
My upload requests
All requests per row security, with status Awaiting upload
My upload requests
App admin
All views
All requests
All requests



5. **My Requests**
   - Information to capture in the new request form.
- Mandatory fields depend on the selection of “Type of request” and “Type of item” and the status of the request (fields must be filled to move to “Awaiting approval” and “Awaiting global approval” and “Global approval”)
   - Documentation regarding the behavior of "My Requests".
   - Approval process for submitted requests.
	- On top of role restrictions for action approve, user can only approve when the mandatory fields have been filled


6. **My Cataloging Requests**
   - Documentation on behavior.
   - Option to download requests.

7. **My Upload Requests**
   - Relevant documentation.
   - Download option necessity.

8. **All Requests**
   - Documentation on overall requests behavior.
   - Download functionality.

9. **Request Detail**
   - Functions and requirements for "Translate" and "Generate Description".
These are python scripts triggered by the relevant action 
   - Adding "Related Uploads" and "Related Translations".
This is part of the information fed by the python scripts and that are mandatory to move from “Global approval” to “Ready for upload”

10. **Comments**
    - Functionality of accessing comments.
Comment are appended from for “Add comment” field to “Communication log”. They can be appended from the request view or as mandatory field when transitioning back to an earlier status 

Status
Authorized transitions
Conditions
Actions
Row security
Drafted
Awaiting maintenance approval, Awaiting help
Awaiting maintenance approval only if: Subset of fields is filled. Subset depends on Type of request and Type of item
Move to: see authorized transitions
Can edit: user is request requester, app admin
Can read only: maintenance approver, purchasing approver, global approver, cataloger of the request
Awaiting maintenance approval
Awaiting maintenance approval, Sent back
Sent back requires comment
Move to: see authorized transitions
Can edit: user is request maintenance approver, app admin
Can read only: maintenance approver, purchasing approver, global approver, cataloger of the request
Awaiting purchasing approval
Awaiting purchasing approval, Sent back
Sent back requires comment
Move to: see authorized transitions
Can edit: user is request purchasing approver, app admin
Can read only: maintenance approver, purchasing approver, global approver, cataloger of the request
Awainting cataloging
Awaiting global approval, Sent back, Awaiting review
Sent back requires comment
Move to: see authorized transitions
Translate: python script, button, on click
Generate descriptions: python script, button, on click
Can edit: user is request cataloger, app admin
Can read only: maintenance approver, purchasing approver, global approver, cataloger of the request
Awaiting global approval
Awaiting upload, Awainting cataloging, Sent back
Awaiting maintenance approval only if: Subset of fields is filled. Subset depends on Type of request and Type of item
Sent back requires comment
Move to: see authorized transitions
Generate xml: python script, on transition to Awaiting upload
Can edit: user is request global approver, app admin
Can read only: maintenance approver, purchasing approver, global approver, cataloger of the request
Awaiting upload
Created, Complete


Move to: see authorized transitions
Can edit: user is request CMMS administrator, app admin
Can read only: maintenance approver, purchasing approver, global approver, cataloger of the request
Created
Complete


Move to: see authorized transitions
Can edit: user is request cataloger, app admin
Can read only: maintenance approver, purchasing approver, global approver, cataloger of the request
Complete






All can read only
Sent back
Awaiting maintenance approval, Awaiting help
Awaiting maintenance approval only if: Subset of fields is filled. Subset depends on Type of request and Type of item
Move to: see authorized transitions
Same as Drafted
Awaiting review
Awainting cataloging, Awaiting global approval


Move to: see authorized transitions
Same as Awaiting global approval
Awaiting help
Sent back


Move to: see authorized transitions
Same as Awaiting cataloging
Canceled






All can read only


    - Visibility and editability of comments.

11. **Edit Request**
    - Editable aspects of a request.
    - Restrictions or permissions for editing.

12. **My Approvals, Search, Filter, Multiple Selector, Sync**
    - Various functionalities, requirements, and documentation related to approvals, searching, filtering, selecting multiple items, and data synchronization.
13. Milestones

Phase
Milestone
Description
% of Total Price Paid
1
Milestone 1
Core Authentication
10%
1
Milestone 2
Role-Based Access Control and User Roles
30%
1
Milestone 3
Request Management System
30%
1
Milestone 4
User Experience (UX) and Interface Design
30%



Phase
Milestone
Description
% of Total Price Paid
2
Milestone 5
User Registration
20%
2
Milestone 6
Users Management
50%
2
Milestone 7
Application Infrastructure
25%
2
Milestone 8
Advanced Features and Integrations
20%


Milestone 1: Core Authentication

1. **User Login**:
   - Implement basic email and password login.
   - Integrate Single Sign-On (SSO) with Google/Microsoft accounts.
   
2. **Forget/Reset Password**:
   - Setup a system for password resets via email links.

3. **Security**:
   - Ensure HTTPS is implemented.

**Deliverables**: A secure authentication system supporting SSO, with a process for password management, detailed documentation

Milestone 2: Role-Based Access Control and User Roles

1. **Define User Roles and Permissions**:
   - Implement the roles as defined (App admin, Requester, Various Approvers, Cataloger, CMMS administrator).
   - Setup view and edit permissions based on roles.

**Deliverables**: A fully functional role-based user experiences and access rights according to defined roles, detailed documentation
Milestone 3: Request Management System

1. **My Requests**:
   - Implement the form for new requests with conditional mandatory fields.
   - Develop the backend logic for the approval process.

2. **My Cataloging Requests** & **My Upload Requests**:
   - Setup interfaces and backend logic for cataloging and upload requests, including download options.

3. **All Requests & Request Detail**:
   - Create views for all requests with detailed views including functionalities like "Translate", "Generate Description", adding "Related Uploads", and "Related Translations".

4. **Comments System**:
   - Develop the comments system, including visibility and editability based on user roles and request status.

**Deliverables**: A comprehensive request management system allowing users to submit, view, and manage requests with an integrated approval workflow, detailed documentation

Milestone 4: User Experience (UX) and Interface Design

1. Ensuring that UX/UI design match with template 

2. Mobile and laptop user experience 

**Deliverables**: same look and feel as the application in AppSheet on laptop and mobile
Milestone  5: User registration

3. **User Registration**:
   - Develop a registration flow with email verification.
   - Implement admin or global approver activation workflow.

4. **Security**:
   - Plan for future Multi-Factor Authentication (MFA) integration.

**Deliverables**: A secure authentication system supporting SSO, with a process for user registration and password management, detailed documentation
Milestone 6: Users management

1. **User Roles Management Interface**:
   - Create an admin interface for assigning and managing user roles.

**Deliverables**: A fully functional role-based access control system tailoring user experiences, detailed documentation
Milestone 7: Application Infrastructure
0. Migrate from Azure App Services to Azure Ubuntu VM

1. **Testing and CI/CD**:
   - Establish a testing suite for backend and frontend.
   - Setup a CI/CD pipeline for automatic testing and deployment.

2. **Performance Monitoring, Logging, and Alerting**:
   - Integrate tools for monitoring application performance and errors.
   - Set up alerting for critical incidents and errors in the application to ensure that any issues can be promptly addressed.

3. **Backup and Disaster Recovery**:
   - Implement regular backup strategies and a disaster recovery plan.

**Deliverables**: A stable, secure, and efficiently deployable application with monitoring and backup strategies in place, as well as alerts, hosted on Azure Ubuntu VM, detailed documentation
Milestone 8: Advanced Features and Integrations

1. **Social Media Login Integration**:
   - Extend SSO capabilities to include social media accounts.

2. **Enhanced Security Features**:
   - Add support for MFA.
   - Implement Web Application Firewall (WAF) and vulnerability scanning.

3. **Data Protection Compliance**:
   - Ensure GDPR compliance in user data handling and registration processes.
   - Communicate the terms of service and privacy policy

**Deliverables**: Expanded authentication options, enhanced security measures, and compliance with data protection regulations, acknowledgement of terms and conditions, detailed documentation

13. Revision log
Version 0.3:
Added: primary goal and Azure App Services / Azure Ubuntu VM
Version 0.2:
Added: technology stack, milestones, revision log
Version 0.1: 
Creation
