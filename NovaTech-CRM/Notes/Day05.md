# Day 5 - Permission Sets and Access Extension

## Objective

Grant additional permissions to selected Sales Representatives without changing the baseline Sales profile.

## Configuration

Created **Senior Sales Rep Access** Permission Set.

Additional access granted:

- Annual Revenue: Read + Edit
- Account: Delete

Assigned the Permission Set to:

- User: Alex Johnson
- Profile: Custom: Sales Profile
- Role: Sales Representative

Regular Sales Representatives continue to use the baseline permissions from the Custom: Sales Profile.

## Concepts Learned

- **Profile** - provides baseline user permissions.
- **Permission Set** - grants additional permissions to selected users.
- **Permission Set Group** - bundles multiple Permission Sets.
- **Muting Permission Set** - mutes selected permissions within a Permission Set Group.
- **Role** - helps determine record access through the role hierarchy.

## Key Learning

Permission Sets are additive. They allow an Admin to provide additional access to selected users without modifying the permissions of every user assigned to the same Profile.

## Result

Successfully extended the NovaTech security model by providing additional Account permissions to a selected Sales Representative.

**Status: Complete**