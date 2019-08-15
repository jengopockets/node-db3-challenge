# Database Queries

### Display the ProductName and CategoryName for all products in the database. Shows 76 records.

SELECT ProductName as Name, Categories.CategoryName as Category
FROM Products
INNER JOIN Categories ON Products.CategoryID = Categories.CategoryID


### Display the OrderID and ShipperName for all orders placed before January 9, 1997. Shows 161 records.

SELECT  OrderID, Shippers.ShipperName, OrderDate 
FROM [Orders]
inner JOIN Shippers ON Orders.ShipperID = Shippers.ShipperID

WHERE OrderDate < '1997-01-09';

### Display all ProductNames and Quantities placed on order 10251. Sort by ProductName. Shows 3 records.

SELECT  OrderID, Products.ProductName, Quantity
FROM [OrderDetails]
inner JOIN Products ON OrderDetails.ProductID = Products.ProductID
WHERE OrderID = 10251

### Display the OrderID, CustomerName and the employee's LastName for every order. All columns should be labeled clearly. Displays 196 records.

SELECT  OrderID, Customers.CustomerName, Employees.LastName
FROM Orders
INNER JOIN Customers ON Orders.CustomerID = Customers.CustomerID
INNER JOIN Employees ON Orders.EmployeeID = Employees.EmployeeID


### (Stretch)  Displays CategoryName and a new column called Count that shows how many products are in each category. Shows 9 records.

### (Stretch) Display OrderID and a  column called ItemCount that shows the total number of products placed on the order. Shows 196 records. 