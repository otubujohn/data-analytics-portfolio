# Project Brief

## Stakeholder
Retail executive and operations leadership.

## Business problem
Identify the drivers of sales, profit, returns, discount losses, and shipping performance.

## Questions
1. Which regions and categories produce the most sales and profit?
2. Which high-sales products are unprofitable?
3. How are discount levels associated with profit margin?
4. Which subcategories have the highest return rates?
5. How does shipping performance differ by region and ship mode?


## Data Grain

- Orders: one row represents one product line within a customer order.
- Returns: one row represents one returned Order ID.
- People: one row represents one regional manager assignment.

## Planned Relationships

- Orders.Order ID will be matched with Returns.Order ID.
- Orders.Region will be matched with People.Region.
- Orders will remain the primary table.
- Both joins will use a left outer join so that all 10,194 order-line records are preserved.

## Expected Merge Validation

- Rows before Returns merge: 10,194
- Rows after Returns merge: 10,194
- Rows after People merge: 10,194