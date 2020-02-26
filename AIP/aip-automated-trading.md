# AIP-2

###### tags: `AIP` `Project` `Engineering` `Application`

## Simple Summary
Desktop app for trading automation with the ability to create markets in one click.

## Abstract
Liquidity is one of the most important components of UX. The presence of open automated systems will significantly reduce the entry threshold for market makers, which will lead to an increase in liquidity.

## Motivation
At the moment, there are big problems with liquidity on the platform. Those few market makers work in the red. The complete lack of tools for automated trading.

## Definition  of Done
*Open source desktop application. Add code to the OracleDAO repo.

## Specification
1. Desktop application;
2. Connect to Betfair API using Betfair Application Key (the user must independently generate a key on the Betfair website);
3. Connect to Ethereum network using Infura or local client (the user must independently generate a key on the Infura website);
4. 0x stuff (have no idea how it works);
5. Market creation section;
5.1 Creating a treeview using Betfair API call: sport / league / event (similar to how it is done on the Betfair website);
5.2 Moving through the list, the user can mark the events of interest to him using the checkbox;
5.3 Having marked the events, the user clicks the "Create market(s)" button;
5.4 The user moves to the next page, where it will be necessary to mark the type of market being created. Types of markets:
- "Moneyline" matches the Augur templates Football (Soccer) / Multiple Choice / Men's Football (Soccer): Which team will win: [Team A] vs. [Team B]?;

//some work needs to be done comparing market types with Augur templates, will be done later.

5.5 After everything is done, the user clicks the button "Publish the market(s)", after which the templates are automatically filled and transactions are automatically signed;
6. Trading section;
6.1 Search for markets on Augur created using templates and matching them with similar markets on Betfair;
6.2 Market selections, setting the desired spread, liquidity, time and conditions of exit from the market, etc.;

//formulas and more will be added later.

6.3 The bot keeps the spread (moving orders), replenishes liquidity if necessary, hedges (on Betfair) matched (on Augur) orders.
6.4 Leaves the market before "n" minutes (user-set time) before the start of the event.

## Costs
Have no idea.

## Rationale
This is a rough sketch, I hope the others will help polish this AIP.
