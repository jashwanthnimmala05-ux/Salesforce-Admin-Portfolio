# Day 4 - Salesforce Security and Access Control

## Objective

Configure a secure access model for NovaTech Sales Representatives using Salesforce security features.

## 1. Field-Level Security

Configured the **Custom: Sales Profile** to control access to Account fields.

### Annual Revenue
- Visible: Yes
- Read-Only: Yes
- Sales Representatives can view the field but cannot modify it.

### SLA Serial Number
- Visible: No
- Sales Representatives cannot access the field.

## 2. Account Object Permissions

Configured Account permissions for the Custom: Sales Profile:

- Read: Yes
- Create: Yes
- Edit: Yes
- Delete: No
- View All: No
- Modify All: No

This allows Sales Representatives to work with Accounts without allowing them to delete records.

## 3. Organization-Wide Defaults

Changed Account internal access from **Public Read/Write** to **Private**.

This establishes a restrictive record-access baseline so users do not automatically receive access to every Account.

## 4. Role Hierarchy

Configured the following hierarchy:

CEO
└── COO
    └── Sales Manager
        └── Sales Representative

This supports hierarchical record access between Sales Representatives and management.

## 5. Test User

Created a dedicated Sales Representative test user:

- User: Alex Johnson
- Profile: Custom: Sales Profile
- Role: Sales Representative

The user will be reused for future security testing.

## Key Learning

Salesforce security operates at different levels:

- **Object-Level Security** — controls what actions users can perform on an object.
- **Field-Level Security** — controls which fields users can view or edit.
- **Record-Level Security** — controls which individual records users can access.
- **Profiles** define baseline user permissions.
- **Roles and sharing mechanisms** help determine record visibility.

## Result

Successfully implemented the initial NovaTech security model using Field-Level Security, Object Permissions, Organization-Wide Defaults, and Role Hierarchy.

**Status: Complete**