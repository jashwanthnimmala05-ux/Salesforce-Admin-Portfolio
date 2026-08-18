# Day 2 - Account Configuration

## Business Requirement
NovaTech Sales needs additional Account information to prioritize customers and track customer relationships and contract dates.

## Configuration

| Field | Type | Purpose |
|---|---|---|
| Customer Relationship | Picklist | Track current relationship with Account |
| Renewal Date | Date | Track upcoming contract renewal |
| Strategic Account | Checkbox | Identify strategically important customers |
| Customer Since | Date | Track beginning of customer relationship |

Used the standard `Employees` field instead of creating a duplicate custom field.

## Test Record
**Account:** ABC Manufacturing

- Employees: 500
- Customer Priority: High
- Customer Relationship: Active Customer
- Renewal Date: 12/15/2026
- Strategic Account: True
- Customer Since: 08/01/2026

## Testing
Verified fields were visible on the Account page layout and values could be saved successfully.

**Result:** PASS

## Key Learning
Before creating custom fields, verify whether Salesforce already provides an appropriate standard field.

Field visibility troubleshooting:
Field-Level Security → Page Layout → Layout Assignment → Refresh/Hard Refresh.