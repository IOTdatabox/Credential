### Blockchain / Web3 ###

1) Gempad.app (Next.js, Solidity/Hardhat, Rust/Anchor) - A revolutionary multichain decentralized launchpad designed to provide a secure and transparent environment for project owners to initiate funding rounds for their tokens, while offering contributors a safe and seamless platform to participate in these sales.
-	Wrote smart contracts for EVM based networks and solana programs
-	Built UI components from the UI/UX design given and writing smart contract codes.
-	Released versions: testnet.gempad.app, legacy.gempad.app, gempad.app, 

I am going to explain my experience related to presale / locks / stacking etc. I started this project from 4 years ago. That was just legacy version (legacy.gempad.app) Now the current version V2 (gempad.app) has wonderful functionalities of presale, locks, stacking, OTC sale (I suggested this idea to my client, maybe other launchpads will never have this function), bridge. Especially, presale field will catch your eyes. I set the values softcap and hardcap, and gempoints. If someone has enough gempoints, he/she can be registered as whiltelist, so that the wallets enlisted in whiltelist can take part in presale stage. This platform provides project owners and token holders with wonderful fundraising services. Most of tokens from EVM based networks have successfully launched now in this platform. Currently, I am on the way to launch Solana version(solsale.app) in the near future.

2) Launchmynft.io (Golang, Rust, CandyMachine, Go-Solana) - A fully automated NFT collection generator that requires no technical knowledge. It offers a simple three-step process: importing assets, setting metadata and rarity, and launching the collection. Users can customize their mint page and promote their NFTs online.

-	Implemented CompressedNFT and programmableNFT by Go-Solana SDKs and Golang
-	Though we have wonderful compressed token management libraries from Metaplex, there is no go-solana sdks for cNFT/pNFT. I implemented the same functionalitis of CandyMachine and cNFT including merkle tree account creation and getting merkle proof using read data api.

I am going to explain about CandyMachine through this experience. You know CM helps us mint NFTs easily. I recently helped them mint compressedNFT (cNFT) using CandyMachine v6, and recently, I tried to implement cNFT again by Golang and go-solana sdks. It worked fine. Of course, Metaplex provides us good examples and libraries for most of CM minting and cNFT, but go-solana sdks don't have such this functionality yet. I was very hard to write pure golang codes like instruction, transaction, metadata args, etc. But you know, the result was that I delivered the project on time. This experience was one of the most challenging what I've encountered so far.

If you'd like these two experince, I'd love to connect and move forward.

### Web Full Stack ###
1)	app.dentalbilling.com | hub.eassist.me – the web portal for eAssist Dental Billing Solution, staffs, dentists, customers, and insurance companies.
eAssist’s clients are dentists who own and run their own dental offices (dental practices). eAssist staff members provide service to these client dentists by billing the insurance companies of the dentist’s patients; as well as collecting payments from the dentist’s patients as well.
-	Required skills: Angular.js 1.x, Node.js, Claudia.js, AWS serverless stack (Lambda, API Gateway, DynamoDB), Lambda (Node.js/Python), SQS/SNS, Cognito
-	My role: First as a front-end developer, after 6 months, as a project manager and full stack developer who is responsible for managing eAssist WoW point system.
-	Day-to-day responsibilities: Interpreting customers’ business requirements, splitting them to smaller ones, assigning subtasks to team members, managing ticket issuing system and VCS (GitHub, Bitbucket), facing customers, resolving issues, mentoring juniors and developing a big rock independently, exactly WoW point system which is evaluating eAssist staff members’ scores.
2)	gempad.app - A revolutionary multichain decentralized launchpad designed to provide a secure and transparent environment for project owners to initiate funding rounds for their tokens, while offering contributors a safe and seamless platform to participate in these sales.
-	Required skills: Rust/Anchor, Ethereum/Solidity/Hardhat, Next.js 13, TailwindCSS, Digital Ocean
-	My role: frontend heavy full stack developer with web3 technologies and deep knowledge of ethereum and solana. (Founding engineer)
-	Day-to-day responsibilities: Building UI components from the UI/UX design given and writing smart contract codes.
3)	salesfuse.io – A workflow management SaaS platform designed to support sales and marketing leaders who are creating sales-specific messages for a global sales team.
-	Required skills: Angular 14/16, Java 11/17, Spring Boot 2.4/3.0, Node.js, AWS EC2, RDS, SSH
-	My role: individual contributor, directly worked with CEO
-	Day-to-day responsibilities: Upgraded the legacy codes and old versions of frameworks and programming languages to the newer ones.
4)	showzong.gg - MLB The Show player database, team builder, flipping tools, card builder, advanced data powered by AI and so much more.
-	Required skills: Next.js 12, Tailwind CSS, Nest.js, TypeORM, AWS
-	My role: individual contributor, worked in a distributed team at full stack developer role.
-	Day-to-day responsibilities: fixing bugs, resolving GitHub issues, managing the AWS EC2 servers, optimizing the databases.
5)	eeginfo.com – A professional training and clinical services company offering hands on clinical training courses by Sue & Siegfried Othmer.
-	Required skills: Java 7/8, Spring Boot 2.2.7 / 2.7+, Hibernate, JSP, Angular 16, React Native, Node.js/Python for Lambda, AWS EC2, Jenkins, GitHub workflow action
-	My role: individual contributor, worked in a distributed team at full stack developer role.
-	Day-to-day responsibilities: Daily commits to GitHub, handling frequent requirement changes in urgent timely manner, fixing issues on GitHub, CI/CD, server management
6)  maxlifeapp.com | maxlifemusic.io | hillsongworship.io - MaxLife Official Fan Club portal which provides private live streams, listening to Lions and Legacy clients' latest music and engage with their fans. their clients (e.g. Hillsong) are all artists.
-   Required skills: Next.js 13, Tailwind CSS, Nest.js , TypeORM, SequelizeORM, GraphQL, Netlify, Godday, AWS EC2, RDS, SSH
-   My role: individual contributor, worked in a distributed team at backend developer role.
-   Day-to-day responsibilities: Developing APIs, maintaining servers on AWS EC2, databases on RDS with SSH tunneling, handling frequent requirement changes in urgent timely manner, fixing issues on GitHub, and CI/CD.
7)  Exitlag.com - ExitLag ensures better and faster connection routes to game servers, eliminating connection issues with a single button press. ExitLag brings an end to Lag, Ping, Packet Loss and Jitter issues by patching you through the optimal route in real time.
-   Required skills: Rust, Golang, Next.js, TailwindCSS, Nest.js, ClickHouse, WebSocket, RabbitMQ, GraphQL
-   My role: I contributed this project from scratch. We'd say exitlag has developed by gamers, for gamers, We implemented a proprietary technology that optimizes data routing by instantaneously mapping out various routes and sending the packet through the optimal one! In case one route becomes unstable, the others kick in keeping the game connection unphased.
-   Day-to-day responsibilities: Developed the latecy monitoring platform with Next.js 13, Nest.js w/ SequelizeORM, and GraphQL. And improved Rust/Golang based serverless backend API codes w/ high demanding microservices.

### Web Full Stack (Java | JS) ###
1)	app.dentalbilling.com | hub.eassist.me – the web portal for eAssist Dental Billing Solution, staffs, dentists, customers, and insurance companies.
eAssist’s clients are dentists who own and run their own dental offices (dental practices). eAssist staff members provide service to these client dentists by billing the insurance companies of the dentist’s patients; as well as collecting payments from the dentist’s patients as well.
-	Required skills: Angular.js 1.x, Spring Boot 2.4/2.7, Java 11/17, Hibernate, JSP, Node.js, Claudia.js, AWS serverless stack (Lambda, API Gateway, DynamoDB), Lambda (Node.js/Python), SQS/SNS, Cognito, Docker, Elasticsearch, Redis, RabbitMQ
-	My role: First as a front-end developer, after 6 months, as a project manager and full stack developer who is responsible for managing eAssist WoW point system.
-	Day-to-day responsibilities: Interpreting customers’ business requirements, splitting them to smaller ones, assigning subtasks to team members, managing ticket issuing system and VCS (GitHub, Bitbucket), facing customers, resolving issues, mentoring juniors and developing a big rock independently, exactly WoW point system which is evaluating eAssist staff members’ scores.
2)	gempad.app - A revolutionary multichain decentralized launchpad designed to provide a secure and transparent environment for project owners to initiate funding rounds for their tokens, while offering contributors a safe and seamless platform to participate in these sales.
-	Required skills: Next.js 13, TailwindCSS, Digital Ocean
-	My role: frontend heavy full stack developer with web3 technologies and deep knowledge of ethereum and solana. (Founding engineer)
-	Day-to-day responsibilities: Building UI components from the UI/UX design given and writing smart contract codes.
3)	salesfuse.io – A workflow management SaaS platform designed to support sales and marketing leaders who are creating sales-specific messages for a global sales team.
-	Required skills: Angular 14/16, Java 11/17, JSP, Spring Boot 2.4/3.0, Hibernate, Node.js, AWS EC2, RDS, SSH
-	My role: individual contributor, directly worked with CEO
-	Day-to-day responsibilities: Upgraded the legacy codes and old versions of frameworks and programming languages to the newer ones.
4)	showzong.gg - MLB The Show player database, team builder, flipping tools, card builder, advanced data powered by AI and so much more.
-	Required skills: Next.js 12, Tailwind CSS, Nest.js, TypeORM, AWS
-	My role: individual contributor, worked in a distributed team at full stack developer role.
-	Day-to-day responsibilities: fixing bugs, resolving GitHub issues, managing the AWS EC2 servers, optimizing the databases.
5)	eeginfo.com – A professional training and clinical services company offering hands on clinical training courses by Sue & Siegfried Othmer.
-	Required skills: Java 7/8, Spring Boot 2.2.7 / 2.7+, Hibernate, JSP, Angular 16, React Native, Node.js/Python for Lambda, AWS EC2, Jenkins, GitHub workflow action
-	My role: individual contributor, worked in a distributed team at full stack developer role.
-	Day-to-day responsibilities: Daily commits to GitHub, handling frequent requirement changes in urgent timely manner, fixing issues on GitHub, CI/CD, server management
6)  maxlifeapp.com | maxlifemusic.io | hillsongworship.io - MaxLife Official Fan Club portal which provides private live streams, listening to Lions and Legacy clients' latest music and engage with their fans. their clients (e.g. Hillsong) are all artists.
-   Required skills: Next.js 13, Tailwind CSS, Nest.js , TypeORM, SequelizeORM, GraphQL, Netlify, Godday, AWS EC2, RDS, SSH
-   My role: individual contributor, worked in a distributed team at backend developer role.
-   Day-to-day responsibilities: Developing APIs, maintaining servers on AWS EC2, databases on RDS with SSH tunneling, handling frequent requirement changes in urgent timely manner, fixing issues on GitHub, and CI/CD.
7)  Exitlag.com - ExitLag ensures better and faster connection routes to game servers, eliminating connection issues with a single button press. ExitLag brings an end to Lag, Ping, Packet Loss and Jitter issues by patching you through the optimal route in real time.
-   Required skills: Next.js, TailwindCSS, Nest.js, ClickHouse, WebSocket, RabbitMQ, GraphQL
-   My role: I contributed this project from scratch. We'd say exitlag has developed by gamers, for gamers, We implemented a proprietary technology that optimizes data routing by instantaneously mapping out various routes and sending the packet through the optimal one! In case one route becomes unstable, the others kick in keeping the game connection unphased.
-   Day-to-day responsibilities: Developed the latecy monitoring platform with Next.js 13, Nest.js w/ SequelizeORM, and GraphQL. And improved Rust/Golang based serverless backend API codes w/ high demanding microservices.

### Web Full Stack (Node | Python | JS) ###
1)	app.dentalbilling.com | hub.eassist.me – the web portal for eAssist Dental Billing Solution, staffs, dentists, customers, and insurance companies.
eAssist’s clients are dentists who own and run their own dental offices (dental practices). eAssist staff members provide service to these client dentists by billing the insurance companies of the dentist’s patients; as well as collecting payments from the dentist’s patients as well.
-	Required skills: Angular.js 1.x, Node.js, Claudia.js, Python, AWS serverless stack (Lambda, API Gateway, DynamoDB), Lambda (Node.js/Python), SQS/SNS, Cognito
-	My role: First as a front-end developer, after 6 months, as a project manager and full stack developer who is responsible for managing eAssist WoW point system.
-	Day-to-day responsibilities: Interpreting customers’ business requirements, splitting them to smaller ones, assigning subtasks to team members, managing ticket issuing system and VCS (GitHub, Bitbucket), facing customers, resolving issues, mentoring juniors and developing a big rock independently, exactly WoW point system which is evaluating eAssist staff members’ scores.
2)	gempad.app - A revolutionary multichain decentralized launchpad designed to provide a secure and transparent environment for project owners to initiate funding rounds for their tokens, while offering contributors a safe and seamless platform to participate in these sales.
-	Required skills: Next.js 13, TailwindCSS, Python, Django, Nest.js, Digital Ocean
-	My role: frontend heavy full stack developer with web3 technologies and deep knowledge of ethereum and solana. (Founding engineer)
-	Day-to-day responsibilities: Building UI components from the UI/UX design given and writing smart contract codes.
3)	salesfuse.io – A workflow management SaaS platform designed to support sales and marketing leaders who are creating sales-specific messages for a global sales team.
-	Required skills: Angular 14/16, Node.js, Express.js, Django, AWS EC2, RDS, SSH
-	My role: individual contributor, directly worked with CEO
-	Day-to-day responsibilities: Upgraded the legacy codes and old versions of frameworks and programming languages to the newer ones.
4)	showzong.gg - MLB The Show player database, team builder, flipping tools, card builder, advanced data powered by AI and so much more.
-	Required skills: Next.js 12, Tailwind CSS, Nest.js, TypeORM, AWS
-	My role: individual contributor, worked in a distributed team at full stack developer role.
-	Day-to-day responsibilities: fixing bugs, resolving GitHub issues, managing the AWS EC2 servers, optimizing the databases.
5)	eeginfo.com – A professional training and clinical services company offering hands on clinical training courses by Sue & Siegfried Othmer.
-	Required skills: Angular 16, React Native, Node.js/Python for Lambda, AWS EC2, Jenkins, GitHub workflow action
-	My role: individual contributor, worked in a distributed team at full stack developer role.
-	Day-to-day responsibilities: Daily commits to GitHub, handling frequent requirement changes in urgent timely manner, fixing issues on GitHub, CI/CD, server management
6)  maxlifeapp.com | maxlifemusic.io | hillsongworship.io - MaxLife Official Fan Club portal which provides private live streams, listening to Lions and Legacy clients' latest music and engage with their fans. their clients (e.g. Hillsong) are all artists.
-   Required skills: Next.js 13, Tailwind CSS, Nest.js , TypeORM, SequelizeORM, GraphQL, Netlify, Godday, AWS EC2, RDS, SSH
-   My role: individual contributor, worked in a distributed team at backend developer role.
-   Day-to-day responsibilities: Developing APIs, maintaining servers on AWS EC2, databases on RDS with SSH tunneling, handling frequent requirement changes in urgent timely manner, fixing issues on GitHub, and CI/CD.
7)  Exitlag.com - ExitLag ensures better and faster connection routes to game servers, eliminating connection issues with a single button press. ExitLag brings an end to Lag, Ping, Packet Loss and Jitter issues by patching you through the optimal route in real time.
-   Required skills: Python/Flask, Next.js, TailwindCSS, Nest.js, ClickHouse, WebSocket, RabbitMQ, GraphQL
-   My role: I contributed this project from scratch. We'd say exitlag has developed by gamers, for gamers, We implemented a proprietary technology that optimizes data routing by instantaneously mapping out various routes and sending the packet through the optimal one! In case one route becomes unstable, the others kick in keeping the game connection unphased.
-   Day-to-day responsibilities: Developed the latecy monitoring platform with Next.js 13, Nest.js w/ SequelizeORM, and GraphQL. And improved Rust/Golang based serverless backend API codes w/ high demanding microservices.