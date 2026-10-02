# SQL Filters

Practice with filtering data in SQL using `WHERE`, `AND`, `OR`, `NOT`, and `LIKE`. 

This was a Coursera lab where I investigated login attempts and prepared security updates for employee machines.

The full write-up with queries and screenshots is in [Apply filters to SQL queries](apply-filters-to-sql-queries.md).

## What I practiced

- Filtering rows with `WHERE`
- Combining conditions with `AND`, `OR`, and `NOT`
- Matching patterns with `LIKE` and the `%` wildcard

## Tasks

| # | Task | Filters used | Rows returned |
|---|------|--------------|---------------|
| 1 | Retrieve after hours failed login attempts | `AND` | 19 |
| 2 | Retrieve login attempts on specific dates | `OR` | 75 |
| 3 | Retrieve login attempts outside of Mexico | `NOT`, `LIKE` | 144 |
| 4 | Retrieve employees in Marketing | `AND`, `LIKE` | 7 |
| 5 | Retrieve employees in Finance or Sales | `OR` | 71 |
| 6 | Retrieve all employees not in IT | `NOT` | 161 |

## Example

```sql
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00' AND success = 0;
```

This query returns the failed login attempts made after business hours.