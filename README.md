# Northwind Services

## Project Overview

Northwind is a fictitious company transferring ad-hoc, identity tracking processes to a structured Entra ID directory instance.

## Business Scenario

Northwind Services is a 16-person company that has been running on shared
logins and a spreadsheet of who has access to what. They are moving to Microsoft
Entra ID and they have hired me to set the directory up properly the first time.

## Tools Used

- Microsoft Entra ID (Free Tier)

## What I Built

Provisioned 16 identities and 6 security groups in Entra ID to represent and organize 16 individuals trusted by Northwind.

## Screenshots
### Users
![Northwind users listed in Entra ID](screenshots/northwind_users@2x.png)
### User Details
![Northwind users listed in Entra ID](screenshots/user_properties@2x.png)
### Groups
![Northwind users listed in Entra ID](screenshots/northwind_groups@2x.png)
### Group Members
![Northwind users listed in Entra ID](screenshots/groupmembers@2x.png)
### Audit Logs
![Entra ID audit logs](screenshots/groupandusermgmt_auditlogs.png)


## Security Lessons Learned

When designing security groups, it is important to consider trade-offs and improvements relative to future growth and expansion. This makes managing groups, users and ultimately, permissions less complex as an organization scales.

## Future Improvements

Leverage dynamic group memberships (requires Entra ID P1). 
Create supplementary documentation that governs group creation and assignment processes.
