# Case Study #1: Danny's Diner

## Context: 
Danny’s Diner is in need of your assistance to help the restaurant stay afloat - the restaurant has captured some very basic data from their few months of operation but have no idea how to use their data to help them run the business.

-- What is the total amount each customer spent at the restaurant? 
SELECT 
	sales.customer_id
    ,SUM(price)
FROM sales
LEFT JOIN menu ON sales.product_id = menu.product_id
GROUP BY sales.customer_id;
