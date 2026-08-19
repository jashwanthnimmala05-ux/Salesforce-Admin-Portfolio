# Day 3 - Account Validation Rules

## Business Problem

NovaTech needs to prevent incomplete or invalid Account data from being saved in Salesforce.

## Validation Rules Implemented

### 1. Active Customer Requires Renewal Date

**Business Rule:**  
Accounts classified as Active Customers must have a Renewal Date.

**Logic:**
- Active Customer + Blank Renewal Date → Block
- Active Customer + Renewal Date → Allow
- Prospect + Blank Renewal Date → Allow

**Result:** PASS

---

### 2. Renewal Date Cannot Be in the Past

**Business Rule:**  
Users cannot enter a Renewal Date earlier than today's date.

**Logic:**
- Past Renewal Date → Block
- Future Renewal Date → Allow
- Blank Renewal Date → Not handled by this rule

**Result:** PASS

---

### 3. Strategic Account Requires Annual Revenue

**Business Rule:**  
Accounts marked as Strategic must contain Annual Revenue.

**Logic:**
- Strategic + Blank Annual Revenue → Block
- Strategic + Annual Revenue → Allow
- Not Strategic + Blank Annual Revenue → Allow

**Result:** PASS

---

## Key Technical Concepts

A Salesforce Validation Rule blocks a save when its formula evaluates to `TRUE`.

`TRUE` = Block  
`FALSE` = Allow

Functions used:

- `AND()` - requires multiple conditions to be true
- `ISPICKVAL()` - evaluates a Picklist value
- `ISBLANK()` - checks whether a field is empty
- `NOT()` - reverses a Boolean condition
- `TODAY()` - returns the current date

Custom fields are referenced using their API names, which commonly end in `__c`.

## Testing

Each validation rule was tested with both positive and negative scenarios.

**Overall Result: PASS**

## Key Learning

Validation Rules enforce data quality at the point of data entry.

A good validation rule should represent a clear business requirement and should be tested against both records that should be blocked and records that should be allowed.