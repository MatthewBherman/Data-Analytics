# Case Study #1: Danny's Diner

## Context: 
Danny’s Diner is facing challenges in maintaining its operations and needs analytical support to utilize its existing data effectively. Over the initial months of operation, the diner has collected basic data but lacks the expertise to analyze this information to enhance business operations.

### Database Schema 

Please see the below tables that I'm using in this process

![Database Schema](/Assets/image.png)

### What is the total amount of sales for each customer?

````sql
SELECT 
  sales.customer_id
  ,SUM(menu.price) AS total_sales
FROM dannys_diner.sales
INNER JOIN dannys_diner.menu
  ON sales.product_id = menu.product_id
GROUP BY sales.customer_id
ORDER BY sales.customer_id ASC; 
````

### 

| Customer | Total Sales |
|-----:|-----------|
|A|76|
|B|74|
|C|36|
