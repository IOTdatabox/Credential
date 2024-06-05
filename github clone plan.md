# Waison
## mobile banking
https://github.com/AWESOME04/Mobile-Bank-Application/


https://github.com/JulieGibbs/etaka

https://github.com/adedayoniyi/Pay-Mobile-P2P-Money-Transfer-App

## p2p
https://github.com/lightningrodlabs/acorn

https://github.com/Power2All/torrust-actix

https://github.com/libp2p/universal-connectivity

https://github.com/FabricLabs/fabric

https://github.com/mxinden/libp2p-lookup

https://github.com/dd-dreams/aft

## portfolio management
https://github.com/gabrielepompa88/pyBlackScholesAnalytics

https://github.com/VivekPa/OptimalPortfolio

https://github.com/open-risk/portfolioAnalytics

https://github.com/nwihardjo/RL-Trading-Agent

## real estate
https://github.com/mde3/casa-crest

## blockchain
https://github.com/ShivaShanmuganathan/NFT-Rental-Marketplace
https://github.com/shashi278/tokenized-realestate


# Aksel (security, java, aws, entertainment, fintech, market analysis, real estate, rental, mortgage)
https://github.com/shawnmckinney/remote-code-execution-sample


https://github.com/greenback-inc/greenback-java

https://github.com/MrLukeKR/Automated-Trader

https://github.com/PhuongDuy/Assignment05

https://github.com/OpreaRazvanVasile/music-Master

https://github.com/rmkasendwa/sliding-tiles

https://github.com/kjanjua26/CommunistBadger

https://github.com/KhouryFinance/awesome-home-buying

https://github.com/ofcyln/mortgage-expense-calculator

https://github.getafreenode.com/Capstoneprolpu/final_Project

https://github.com/microrealestate/microrealestate












Solidity
Java
Javasript
Python
Rust
Go



I need to introduce the idea of the tax table.
Let's start simply.
a. For each source of income, there will be a different tax rate.
b. Income from work = Rate 1
b1. Income from RMDs = Rate 1
c. Income from Social Security = Rate 2.
d. Income for capital gains from individual brokerage accounts will be either Rate 3 or Rate 4
e. The issue is that Rates 1-4 will depend on the SUM of the Incomes.
<!-- Rate 2 depends on not only Income from Social Security but also Income from work? -->
f. Worse, that every state may have a different tax rate for point c, which will depend on zip code.

First, let's start with this basic setup, there will be nuances.
From the diagram, where do you see this entering the schematic (this is why I needed to see your schematic).

The very complicated situation is the following and the reason the schematic MUST be correct.
a. The UI needs to ask how much MONEY in CASH is needed, WITHOUT considering taxes AT ALL.
<!-- [how much MENEY in CASH] means total expense? So far the math is that total cash flow is same with total expense. but this statement hints more much total cash flow than total expense is needed due to tax. -->
b. You are creating possible approaches to the withdrawal from locations, which have different tax rates. The ripple effect will be that the APTC changes due to tax rules, because it entirely depends on the taxable sum of the income sources, NOT the cash available to the person.
<!-- As you can see in subsidy table of google sheet, there are Zipcode, Household members, Household income, etc as inputs. there is no TAX. APTC depends on the taxable sum of the income sources - this statement is out of my knowledge. According to my knowledge from you, APTC is subsidy. and I thought I simply substract it in Mr.X table. -->
c. Due to point b, the JSCORE will be DIFFERENT (let's call it JSCORE#1).
d. Example, let’s say that the person needs 50,000, and has a job that pays 30000. They need 20,000 of CASH. The issue is that withdrawal, in the sequence you have created, minimizes the tax, intentionally. The ACTUAL reason is that it MINIMIZES the taxable income, which MAXIMIZES the APTC simultaneously.
e. That said, it can be more complicated in situations if the person is above 59.5 and has no cash available. In that instance, then the selling of stocks may result in a taxable amount due to capital gains taxes (point d).
<!-- Is 59.5 a special age? The concept of [selling of stocks] has never been mentioned so far. -->
What I would do is the following:
1. Create a reference table of tax rates that mimics Rate 1-Rate 4. Note that this temporary, we may need ENTIRELY ADDITIONAL links to APIs to retrieve the correct table of rates and process here, that is why the SCHEMATIC must be right.
2. The issue is that since the taxes increase the amount of point a (so we have cash1 for use on food, and another total, call it cash2 for the tax bill.
<!-- User input will be cash1, but we need to know cash 2 - It's the idea of this statement? -->
3. The result is that the number of iterations now EXPLODES, similar to “Goal Seek” on Excel.

This is an incomplete description itself, first you need to understand this document.


