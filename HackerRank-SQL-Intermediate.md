# HackerRank-SQL-Intermediate
HackerRank SQL Intermediate Certification Test Solution
- Product Without Sales
- Business Expansion

## Product Without Sales
```yaml
SELECT p.sku, p.product_name FROM Product p
LEFT JOIN Invoice_item i ON i.product_id = p.id
WHERE i.invoice_id IS NULL
```

## Business Expansion
```yaml
SELECT u.id, u.first_name, u.last_name, c.id, c.customer_name,COUNT(c.id)
FROM Customer c, User_account u, Contact c1
WHERE c.id = c1.customer_id AND c1.user_account_id = u.id
GROUP BY u.id, u.first_name, u.last_name, c.id, c.customer_name
HAVING COUNT(c.id) > 1
```
