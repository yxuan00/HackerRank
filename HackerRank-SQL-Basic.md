# HackerRank-SQL-Basic
HackerRank SQL Basic Certification Test Solution
- Merit Rewards
- Profitable Stocks

## Merit Rewards
```yaml
SELECT e.employee_ID, e.name FROM Employee_information e 
INNER JOIN Last_quarter_bonus l ON e.employee_ID = l.employee_ID 
WHERE e.division = 'HR' AND l.bonus >= 5000
```

## Profitable Stocks
```yaml
SELECT p.stock_code FROM price_today p
INNER JOIN price_tomorrow pt ON p.stock_code = pt.stock_code
WHERE pt.price > p.price
```
