# answer.sql-week-4

-- Question 1
SELECT paymentDate, SUM(amount) 
FROM payments
GROUP BY paymentDate
ORDER BY paymentDate DESC
LIMIT 5;
-- Question 2
SELECT customerName, country, AVG (creditLimit) 
FROM customers
GROUP BY customerName, country;
-- Question 3
SELECT productCode, quantityOrdered, SUM(quantityOrdered * priceEach) AS totalPrice 
FROM orderdetails
GROUP BY productCode, quantityOrdered;
-- Question 4
SELECT checkNumber, MAX(amount) AS highestAmount
FROM payments
GROUP BY checkNumber;
