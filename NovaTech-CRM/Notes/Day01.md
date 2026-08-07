# Day 1 - Salesforce CRM Foundation

## Project
NovaTech CRM Implementation

## Business Scenario
NovaTech Solutions is a B2B software company using Salesforce to organize customer information, track sales opportunities, and improve visibility into the sales pipeline.

## Core Salesforce Objects

### Lead
A potential customer who has shown interest but has not yet been qualified.

### Account
A company or organization that NovaTech does business with.

### Contact
An individual person associated with an Account.

### Opportunity
A potential sale or revenue-generating deal.

## Records Created

- Lead: Rahul Patel - ABC Manufacturing
- Account: ABC Manufacturing
- Contact: Rahul Patel
- Opportunity: ABC Manufacturing CRM Project

## Relationships Learned

- One Account can have multiple Contacts.
- One Account can have multiple Opportunities.
- A Lead is kept separate while the prospect is still being qualified.
- Accounts represent organizations.
- Contacts represent individual people.
- Opportunities represent potential sales.

## Scenario Learning

If Rahul leaves ABC Manufacturing and joins another organization, how his Contact record is handled depends on the company's data-management policy.

In many implementations, the existing Contact may be updated to the new Account to avoid unnecessary duplicates and preserve relevant history.

## Key Takeaway

Salesforce is not simply a place to store customer information. It organizes relationships between companies, people, prospects, and potential revenue.