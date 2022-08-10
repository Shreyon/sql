1.)	 Display snum,sname,city and comm of all salespeople.

CREATE TABLE Salespeople (

    Snum INT NOT NULL PRIMARY KEY,
    Sname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Comm FLOAT
);

INSERT INTO Salespeople VALUES
    (1001,'Peel','London',0.12),
    (1002,'Serres','San Jose',0.13),
    (1004,'Motika','London',0.11),
    (1007,'Rafkin','Barcelona',0.15),
    (1003,'Axelrod','New york',0.1).

SELECT Snum, Sname, City, Comm
FROM Salespeople.


(2.)	 Display all snum without duplicates from all orders.
CREATE TABLE Orders (
 Onum INT NOT NULL,
    AMT FLOAT NOT NULL,
    Odate DATE NOT NULL,
    Cnum INT NOT NULL,
    Snum INT NOT NULL,
    CONSTRAINT PK_Orders_Onum PRIMARY KEY(Onum),
    CONSTRAINT FK_Orders_Cnum FOREIGN KEY(Cnum) REFERENCES Customers (Cnum),
    CONSTRAINT FK_Orders_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);
INSERT INTO Orders VALUES
    (3001,18.69,'03-OCT-94',2004,1007),
    (3003,767.19,'03-OCT-94',2001,1001),
    (3002,1900.10,'03-OCT-94',2007,1004),
    (3005,5160.45,'03-OCT-94',2003,1002),
    (3006,1098.16,'04-OCT-94',2004,1007),
    (3009,1713.23,'04-OCT-94',2002,1003),
    (3007,75.75,'05-OCT-94',2004,1002),
    (3008,4723.00,'05-OCT-94',2006,1001),
    (30010,1309.95,'06-OCT-94',2004,1002),
    (30011,9891.88,'06-OCT-94',2006,1001).
SELECT DISTINCT Snum
FROM Orders.


(3.)	 Display names and commissions of all salespeople in London.

CREATE TABLE Salespeople (

    Snum INT NOT NULL PRIMARY KEY,
    Sname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Comm FLOAT
);
GO

INSERT INTO Salespeople VALUES
    (1001,'Peel','London',0.12),
    (1002,'Serres','San Jose',0.13),
    (1004,'Motika','London',0.11),
    (1007,'Rafkin','Barcelona',0.15),
    (1003,'Axelrod','New york',0.1).

SELECT Snum, Comm
FROM Salespeople
WHERE City = 'London’.
GO



(4.)	 All customers with rating of 100.

CREATE TABLE Customers (

    Cnum INT NOT NULL,
    Cname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Rating INT,
    Snum INT NOT NULL,
    CONSTRAINT PK_Customers_Cnum PRIMARY KEY(Cnum),
    CONSTRAINT FK_Customers_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Customers
VALUES 
    (2001,'Hoffman','London',100,1001),
    (2002,'Giovanne','Rome',200,1003),
    (2003,'Liu','San Jose',300,1002),
    (2004,'Grass','Brelin',100,1002),
    (2006,'Clemens','London',300,1007),
    (2007,'Pereira','Rome',100,1004).

SELECT Cname 
FROM Customers
WHERE Rating = 100.



(5.)	 Produce orderno, amount and date form all rows in the order table.

CREATE TABLE Orders (

    Onum INT NOT NULL,
    AMT FLOAT NOT NULL,
    Odate DATE NOT NULL,
    Cnum INT NOT NULL,
    Snum INT NOT NULL,
    CONSTRAINT PK_Orders_Onum PRIMARY KEY(Onum),
    CONSTRAINT FK_Orders_Cnum FOREIGN KEY(Cnum) REFERENCES Customers (Cnum),
    CONSTRAINT FK_Orders_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Orders VALUES
    (3001,18.69,'03-OCT-94',2004,1007),
    (3003,767.19,'03-OCT-94',2001,1001),
    (3002,1900.10,'03-OCT-94',2007,1004),
    (3005,5160.45,'03-OCT-94',2003,1002),
    (3006,1098.16,'04-OCT-94',2004,1007),
    (3009,1713.23,'04-OCT-94',2002,1003),
    (3007,75.75,'05-OCT-94',2004,1002),
    (3008,4723.00,'05-OCT-94',2006,1001),
    (30010,1309.95,'06-OCT-94',2004,1002),
    (30011,9891.88,'06-OCT-94',2006,1001).

SELECT Onum, AMT, Odate
FROM Orders.



6. All customers in San Jose, who have rating more than 200

CREATE TABLE Customers (

    Cnum INT NOT NULL,
    Cname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Rating INT,
    Snum INT NOT NULL,
    CONSTRAINT PK_Customers_Cnum PRIMARY KEY(Cnum),
    CONSTRAINT FK_Customers_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Customers VALUES 
    (2001,'Hoffman','London',100,1001),
    (2002,'Giovanne','Rome',200,1003),
    (2003,'Liu','San Jose',300,1002),
    (2004,'Grass','Brelin',100,1002),
    (2006,'Clemens','London',300,1007),
    (2007,'Pereira','Rome',100,1004).

SELECT Cname, City, Rating
FROM Customers
WHERE City = 'San Jose' AND Rating > 200.


7. All customers who were either located in San Jose or had a rating above 200

CREATE TABLE Customers (

    Cnum INT NOT NULL,
    Cname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Rating INT,
    Snum INT NOT NULL,
    CONSTRAINT PK_Customers_Cnum PRIMARY KEY(Cnum),
    CONSTRAINT FK_Customers_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Customers VALUES 
    (2001,'Hoffman','London',100,1001),
    (2002,'Giovanne','Rome',200,1003),
    (2003,'Liu','San Jose',300,1002),
    (2004,'Grass','Brelin',100,1002),
    (2006,'Clemens','London',300,1007),
    (2007,'Pereira','Rome',100,1004).

SELECT Cname, City, Rating
FROM Customers
WHERE City = 'San Jose' OR Rating > 200.
GO

8. All orders for more than $1000.

CREATE TABLE Orders (

    Onum INT NOT NULL,
    AMT FLOAT NOT NULL,
    Odate DATE NOT NULL,
    Cnum INT NOT NULL,
    Snum INT NOT NULL,
    CONSTRAINT PK_Orders_Onum PRIMARY KEY(Onum),
    CONSTRAINT FK_Orders_Cnum FOREIGN KEY(Cnum) REFERENCES Customers (Cnum),
    CONSTRAINT FK_Orders_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Orders VALUES
    (3001,18.69,'03-OCT-94',2004,1007),
    (3003,767.19,'03-OCT-94',2001,1001),
    (3002,1900.10,'03-OCT-94',2007,1004),
    (3005,5160.45,'03-OCT-94',2003,1002),
    (3006,1098.16,'04-OCT-94',2004,1007),
    (3009,1713.23,'04-OCT-94',2002,1003),
    (3007,75.75,'05-OCT-94',2004,1002),
    (3008,4723.00,'05-OCT-94',2006,1001),
    (30010,1309.95,'06-OCT-94',2004,1002),
    (30011,9891.88,'06-OCT-94',2006,1001).

SELECT *
FROM Orders
WHERE AMT > 1000.


9. Names and cites of all salespeople in London with commission above 0.10.

CREATE TABLE Salespeople (

    Snum INT NOT NULL PRIMARY KEY,
    Sname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Comm FLOAT
);

INSERT INTO Salespeople VALUES
    (1001,'Peel','London',0.12),
    (1002,'Serres','San Jose',0.13),
    (1004,'Motika','London',0.11),
    (1007,'Rafkin','Barcelona',0.15),
    (1003,'Axelrod','New york',0.1).

SELECT Sname, City, Comm
FROM Salespeople
WHERE City = 'London' AND Comm > 0.10.


10. All customers excluding those with rating <= 100 unless they are located in Rome.


CREATE TABLE Customers (

    Cnum INT NOT NULL,
    Cname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Rating INT,
    Snum INT NOT NULL,
    CONSTRAINT PK_Customers_Cnum PRIMARY KEY(Cnum),
    CONSTRAINT FK_Customers_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Customers VALUES 
    (2001,'Hoffman','London',100,1001),
    (2002,'Giovanne','Rome',200,1003),
    (2003,'Liu','San Jose',300,1002),
    (2004,'Grass','Brelin',100,1002),
    (2006,'Clemens','London',300,1007),
    (2007,'Pereira','Rome',100,1004);

SELECT Cname, City, Rating
FROM Customers
WHERE Rating <= 100 OR City = 'Rome’.


(11.) All salespeople either in Barcelona or in London.

CREATE TABLE Salespeople (

    Snum INT NOT NULL PRIMARY KEY,
    Sname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Comm FLOAT
);

INSERT INTO Salespeople VALUES
    (1001,'Peel','London',0.12),
    (1002,'Serres','San Jose',0.13),
    (1004,'Motika','London',0.11),
    (1007,'Rafkin','Barcelona',0.15),
    (1003,'Axelrod','New york',0.1).


SELECT Sname, City
FROM Salespeople
WHERE City IN ('Barcelona’, ‘London').


(12.) All salespeople with commission between 0.10 and 0.12.

CREATE TABLE Salespeople (

    Snum INT NOT NULL PRIMARY KEY,
    Sname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Comm FLOAT
);
GO

INSERT INTO Salespeople VALUES
    (1001,'Peel','London',0.12),
    (1002,'Serres','San Jose',0.13),
    (1004,'Motika','London',0.11),
    (1007,'Rafkin','Barcelona',0.15),
    (1003,'Axelrod','New york',0.1).

SELECT Sname, Comm
FROM Salespeople
WHERE Comm > 0.10 AND Comm < 0.12.

(13.) All customers with NULL values in city column.

CREATE TABLE Customers (

    Cnum INT NOT NULL,
    Cname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Rating INT,
    Snum INT NOT NULL,
    CONSTRAINT PK_Customers_Cnum PRIMARY KEY(Cnum),
    CONSTRAINT FK_Customers_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Customers VALUES 
    (2001,'Hoffman','London',100,1001),
    (2002,'Giovanne','Rome',200,1003),
    (2003,'Liu','San Jose',300,1002),
    (2004,'Grass','Brelin',100,1002),
    (2006,'Clemens','London',300,1007),
    (2007,'Pereira','Rome',100,1004).

SELECT Cname, City
FROM Customers
WHERE City IS NULL.


(14.) All orders taken on Oct 3Rd and Oct 4th, 1994.

CREATE TABLE Orders (

    Onum INT NOT NULL,
    AMT FLOAT NOT NULL,
    Odate DATE NOT NULL,
    Cnum INT NOT NULL,
    Snum INT NOT NULL,
    CONSTRAINT PK_Orders_Onum PRIMARY KEY(Onum),
    CONSTRAINT FK_Orders_Cnum FOREIGN KEY(Cnum) REFERENCES Customers (Cnum),
    CONSTRAINT FK_Orders_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Orders VALUES
    (3001,18.69,'03-OCT-94',2004,1007),
    (3003,767.19,'03-OCT-94',2001,1001),
    (3002,1900.10,'03-OCT-94',2007,1004),
    (3005,5160.45,'03-OCT-94',2003,1002),
    (3006,1098.16,'04-OCT-94',2004,1007),
    (3009,1713.23,'04-OCT-94',2002,1003),
    (3007,75.75,'05-OCT-94',2004,1002),
    (3008,4723.00,'05-OCT-94',2006,1001),
    (30010,1309.95,'06-OCT-94',2004,1002),
    (30011,9891.88,'06-OCT-94',2006,1001).

SELECT *
FROM Orders
WHERE Odate IN ('03-OCT-94','04-OCT-94').


(15.) All customers serviced by peel or Motika

CREATE TABLE Salespeople (

    Snum INT NOT NULL PRIMARY KEY,
    Sname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Comm FLOAT
);

INSERT INTO Salespeople VALUES
    (1001,'Peel','London',0.12),
    (1002,'Serres','San Jose',0.13),
    (1004,'Motika','London',0.11),
    (1007,'Rafkin','Barcelona',0.15),
    (1003,'Axelrod','New york',0.1).

SELECT Cname
FROM Customers, Orders
WHERE Orders.Cnum = Customers.Cnum 
AND Orders.Snum IN (SELECT Snum FROM Salespeople WHERE Sname IN ('Peel','Motika')).


(16.) All customers whose names begin with a letter from A to B.

CREATE TABLE Customers (

    Cnum INT NOT NULL,
    Cname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Rating INT,
    Snum INT NOT NULL,
    CONSTRAINT PK_Customers_Cnum PRIMARY KEY(Cnum),
    CONSTRAINT FK_Customers_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Customers VALUES 
    (2001,'Hoffman','London',100,1001),
    (2002,'Giovanne','Rome',200,1003),
    (2003,'Liu','San Jose',300,1002),
    (2004,'Grass','Brelin',100,1002),
    (2006,'Clemens','London',300,1007),
    (2007,'Pereira','Rome',100,1004).

SELECT Cname
FROM Customers
WHERE Cname LIKE 'A%' OR Cname LIKE 'B%’.


(17.) All orders except those with 0 or NULL value in amt field.

CREATE TABLE Orders (

    Onum INT NOT NULL,
    AMT FLOAT NOT NULL,
    Odate DATE NOT NULL,
    Cnum INT NOT NULL,
    Snum INT NOT NULL,
    CONSTRAINT PK_Orders_Onum PRIMARY KEY(Onum),
    CONSTRAINT FK_Orders_Cnum FOREIGN KEY(Cnum) REFERENCES Customers (Cnum),
    CONSTRAINT FK_Orders_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Orders VALUES
    (3001,18.69,'03-OCT-94',2004,1007),
    (3003,767.19,'03-OCT-94',2001,1001),
    (3002,1900.10,'03-OCT-94',2007,1004),
    (3005,5160.45,'03-OCT-94',2003,1002),
    (3006,1098.16,'04-OCT-94',2004,1007),
    (3009,1713.23,'04-OCT-94',2002,1003),
    (3007,75.75,'05-OCT-94',2004,1002),
    (3008,4723.00,'05-OCT-94',2006,1001),
    (30010,1309.95,'06-OCT-94',2004,1002),
    (30011,9891.88,'06-OCT-94',2006,1001).

SELECT *
FROM Orders
WHERE AMT! = 0 OR AMT IS NOT NULL.


(18.) Count the number of salespeople currently listing orders in the order table

CREATE TABLE Orders (

    Onum INT NOT NULL,
    AMT FLOAT NOT NULL,
    Odate DATE NOT NULL,
    Cnum INT NOT NULL,
    Snum INT NOT NULL,
    CONSTRAINT PK_Orders_Onum PRIMARY KEY(Onum),
    CONSTRAINT FK_Orders_Cnum FOREIGN KEY(Cnum) REFERENCES Customers (Cnum),
    CONSTRAINT FK_Orders_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);
INSERT INTO Orders VALUES
    (3001,18.69,'03-OCT-94',2004,1007),
    (3003,767.19,'03-OCT-94',2001,1001),
    (3002,1900.10,'03-OCT-94',2007,1004),
    (3005,5160.45,'03-OCT-94',2003,1002),
    (3006,1098.16,'04-OCT-94',2004,1007),
    (3009,1713.23,'04-OCT-94',2002,1003),
    (3007,75.75,'05-OCT-94',2004,1002),
    (3008,4723.00,'05-OCT-94',2006,1001),
    (30010,1309.95,'06-OCT-94',2004,1002),
    (30011,9891.88,'06-OCT-94',2006,1001).

SELECT COUNT (DISTINCT Snum) AS 'salespeople currently listing orders'
FROM Orders.


(19.) Largest order taken by each salesperson; date wise.

CREATE TABLE Orders (

    Onum INT NOT NULL,
    AMT FLOAT NOT NULL,
    Odate DATE NOT NULL,
    Cnum INT NOT NULL,
    Snum INT NOT NULL,
    CONSTRAINT PK_Orders_Onum PRIMARY KEY(Onum),
    CONSTRAINT FK_Orders_Cnum FOREIGN KEY(Cnum) REFERENCES Customers (Cnum),
    CONSTRAINT FK_Orders_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Orders VALUES
    (3001,18.69,'03-OCT-94',2004,1007),
    (3003,767.19,'03-OCT-94',2001,1001),
    (3002,1900.10,'03-OCT-94',2007,1004),
    (3005,5160.45,'03-OCT-94',2003,1002),
    (3006,1098.16,'04-OCT-94',2004,1007),
    (3009,1713.23,'04-OCT-94',2002,1003),
    (3007,75.75,'05-OCT-94',2004,1002),
    (3008,4723.00,'05-OCT-94',2006,1001),
    (30010,1309.95,'06-OCT-94',2004,1002),
    (30011,9891.88,'06-OCT-94',2006,1001).

SELECT Snum, Odate, MAX(AMT) AS 'Largest order'
FROM Orders
GROUP BY Odate, Snum
ORDER BY Odate,Snum;

(20.) Largest order taken by each salesperson with order value more than $3000.

CREATE TABLE Orders (

    Onum INT NOT NULL,
    AMT FLOAT NOT NULL,
    Odate DATE NOT NULL,
    Cnum INT NOT NULL,
    Snum INT NOT NULL,
    CONSTRAINT PK_Orders_Onum PRIMARY KEY(Onum),
    CONSTRAINT FK_Orders_Cnum FOREIGN KEY(Cnum) REFERENCES Customers (Cnum),
    CONSTRAINT FK_Orders_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Orders VALUES
    (3001,18.69,'03-OCT-94',2004,1007),
    (3003,767.19,'03-OCT-94',2001,1001),
    (3002,1900.10,'03-OCT-94',2007,1004),
    (3005,5160.45,'03-OCT-94',2003,1002),
    (3006,1098.16,'04-OCT-94',2004,1007),
    (3009,1713.23,'04-OCT-94',2002,1003),
    (3007,75.75,'05-OCT-94',2004,1002),
    (3008,4723.00,'05-OCT-94',2006,1001),
    (30010,1309.95,'06-OCT-94',2004,1002),
    (30011,9891.88,'06-OCT-94',2006,1001).

SELECT Snum, Odate, MAX(AMT) AS 'Largest order'
FROM Orders
WHERE AMT > 3000
GROUP BY Odate, Snum
ORDER BY Odate, Snum;


(21.) Which day had the highest total amount ordered.

CREATE TABLE Orders (

    Onum INT NOT NULL,
    AMT FLOAT NOT NULL,
    Odate DATE NOT NULL,
    Cnum INT NOT NULL,
    Snum INT NOT NULL,
    CONSTRAINT PK_Orders_Onum PRIMARY KEY(Onum),
    CONSTRAINT FK_Orders_Cnum FOREIGN KEY(Cnum) REFERENCES Customers (Cnum),
    CONSTRAINT FK_Orders_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Orders VALUES
    (3001,18.69,'03-OCT-94',2004,1007),
    (3003,767.19,'03-OCT-94',2001,1001),
    (3002,1900.10,'03-OCT-94',2007,1004),
    (3005,5160.45,'03-OCT-94',2003,1002),
    (3006,1098.16,'04-OCT-94',2004,1007),
    (3009,1713.23,'04-OCT-94',2002,1003),
    (3007,75.75,'05-OCT-94',2004,1002),
    (3008,4723.00,'05-OCT-94',2006,1001),
    (30010,1309.95,'06-OCT-94',2004,1002),
    (30011,9891.88,'06-OCT-94',2006,1001).

SELECT Odate, AMT, Snum, Cnum
FROM Orders
WHERE AMT = (SELECT MAX(AMT) FROM Orders).


(22.) count all orders for Oct 3rd.

CREATE TABLE Orders (

    Onum INT NOT NULL,
    AMT FLOAT NOT NULL,
    Odate DATE NOT NULL,
    Cnum INT NOT NULL,
    Snum INT NOT NULL,
    CONSTRAINT PK_Orders_Onum PRIMARY KEY(Onum),
    CONSTRAINT FK_Orders_Cnum FOREIGN KEY(Cnum) REFERENCES Customers (Cnum),
    CONSTRAINT FK_Orders_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Orders VALUES
    (3001,18.69,'03-OCT-94',2004,1007),
    (3003,767.19,'03-OCT-94',2001,1001),
    (3002,1900.10,'03-OCT-94',2007,1004),
    (3005,5160.45,'03-OCT-94',2003,1002),
    (3006,1098.16,'04-OCT-94',2004,1007),
    (3009,1713.23,'04-OCT-94',2002,1003),
    (3007,75.75,'05-OCT-94',2004,1002),
    (3008,4723.00,'05-OCT-94',2006,1001),
    (30010,1309.95,'06-OCT-94',2004,1002),
    (30011,9891.88,'06-OCT-94',2006,1001).

SELECT COUNT (*) AS 'Orders on Oct 3rd'
FROM Orders
WHERE Odate = '03-OCT-94’.


(23.) Count the number of different non-NULL city values in customer’s table.

CREATE TABLE Customers (

    Cnum INT NOT NULL,
    Cname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Rating INT,
    Snum INT NOT NULL,
    CONSTRAINT PK_Customers_Cnum PRIMARY KEY(Cnum),
    CONSTRAINT FK_Customers_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Customers VALUES 
    (2001,'Hoffman','London',100,1001),
    (2002,'Giovanne','Rome',200,1003),
    (2003,'Liu','San Jose',300,1002),
    (2004,'Grass','Brelin',100,1002),
    (2006,'Clemens','London',300,1007),
    (2007,'Pereira','Rome',100,1004).

SELECT COUNT (DISTINCT City)
FROM Customers.


(24.)  Select each customer’s smallest order.

CREATE TABLE Orders (

    Onum INT NOT NULL,
    AMT FLOAT NOT NULL,
    Odate DATE NOT NULL,
    Cnum INT NOT NULL,
    Snum INT NOT NULL,
    CONSTRAINT PK_Orders_Onum PRIMARY KEY(Onum),
    CONSTRAINT FK_Orders_Cnum FOREIGN KEY(Cnum) REFERENCES Customers (Cnum),
    CONSTRAINT FK_Orders_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Orders VALUES
    (3001,18.69,'03-OCT-94',2004,1007),
    (3003,767.19,'03-OCT-94',2001,1001),
    (3002,1900.10,'03-OCT-94',2007,1004),
    (3005,5160.45,'03-OCT-94',2003,1002),
    (3006,1098.16,'04-OCT-94',2004,1007),
    (3009,1713.23,'04-OCT-94',2002,1003),
    (3007,75.75,'05-OCT-94',2004,1002),
    (3008,4723.00,'05-OCT-94',2006,1001),
    (30010,1309.95,'06-OCT-94',2004,1002),
    (30011,9891.88,'06-OCT-94',2006,1001).

SELECT Cnum, MIN(AMT)
FROM Orders
GROUP BY Cnum.


(25.) First customer in alphabetical order whose name begins with G.

CREATE TABLE Customers (

    Cnum INT NOT NULL,
    Cname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Rating INT,
    Snum INT NOT NULL,
    CONSTRAINT PK_Customers_Cnum PRIMARY KEY(Cnum),
    CONSTRAINT FK_Customers_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Customers VALUES 
    (2001,'Hoffman','London',100,1001),
    (2002,'Giovanne','Rome',200,1003),
    (2003,'Liu','San Jose',300,1002),
    (2004,'Grass','Brelin',100,1002),
    (2006,'Clemens','London',300,1007),
    (2007,'Pereira','Rome',100,1004).

SELECT MIN(Cname)
FROM Customers
WHERE Cname LIKE 'G%’.


(26.)  Get the output like "For dd/mm/yy there are orders.

CREATE TABLE Orders (

    Onum INT NOT NULL,
    AMT FLOAT NOT NULL,
    Odate DATE NOT NULL,
    Cnum INT NOT NULL,
    Snum INT NOT NULL,
    CONSTRAINT PK_Orders_Onum PRIMARY KEY(Onum),
    CONSTRAINT FK_Orders_Cnum FOREIGN KEY(Cnum) REFERENCES Customers (Cnum),
    CONSTRAINT FK_Orders_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Orders VALUES
    (3001,18.69,'03-OCT-94',2004,1007),
    (3003,767.19,'03-OCT-94',2001,1001),
    (3002,1900.10,'03-OCT-94',2007,1004),
    (3005,5160.45,'03-OCT-94',2003,1002),
    (3006,1098.16,'04-OCT-94',2004,1007),
    (3009,1713.23,'04-OCT-94',2002,1003),
    (3007,75.75,'05-OCT-94',2004,1002),
    (3008,4723.00,'05-OCT-94',2006,1001),
    (30010,1309.95,'06-OCT-94',2004,1002),
    (30011,9891.88,'06-OCT-94',2006,1001).

SELECT 'For’ (CONVERT (varchar (10), GETDATE (),120)) || 'there are' || COUNT (*) || 'Orders'
FROM Orders
GROUP BY Odate;


(27.)  Assume that each salesperson has a 12% commission. Produce order no., salesperson no., and amount of salesperson’s commission for that order.

CREATE TABLE Orders (

    Onum INT NOT NULL,
    AMT FLOAT NOT NULL,
    Odate DATE NOT NULL,
    Cnum INT NOT NULL,
    Snum INT NOT NULL,
    CONSTRAINT PK_Orders_Onum PRIMARY KEY(Onum),
    CONSTRAINT FK_Orders_Cnum FOREIGN KEY(Cnum) REFERENCES Customers (Cnum),
    CONSTRAINT FK_Orders_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Orders VALUES
    (3001,18.69,'03-OCT-94',2004,1007),
    (3003,767.19,'03-OCT-94',2001,1001),
    (3002,1900.10,'03-OCT-94',2007,1004),
    (3005,5160.45,'03-OCT-94',2003,1002),
    (3006,1098.16,'04-OCT-94',2004,1007),
    (3009,1713.23,'04-OCT-94',2002,1003),
    (3007,75.75,'05-OCT-94',2004,1002),
    (3008,4723.00,'05-OCT-94',2006,1001),
    (30010,1309.95,'06-OCT-94',2004,1002),
    (30011,9891.88,'06-OCT-94',2006,1001).

SELECT Onum, Snum, AMT, AMT * 0.12 AS 'Commission'
FROM Orders
ORDER BY Snum.


(28.)  Find highest rating in each city. Put the output in this form. For the city (city), the highest rating is: (rating).

CREATE TABLE Customers (

    Cnum INT NOT NULL,
    Cname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Rating INT,
    Snum INT NOT NULL,
    CONSTRAINT PK_Customers_Cnum PRIMARY KEY(Cnum),
    CONSTRAINT FK_Customers_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Customers VALUES 
    (2001,'Hoffman','London',100,1001),
    (2002,'Giovanne','Rome',200,1003),
    (2003,'Liu','San Jose',300,1002),
    (2004,'Grass','Brelin',100,1002),
    (2006,'Clemens','London',300,1007),
    (2007,'Pereira','Rome',100,1004).

Select 'For the city (' || City || '), the highest rating is: (' || MAX(Rating) || ')'
FROM Customers
GROUP BY city.

(29.)  Display the totals of orders for each day and place the results in descending order.

CREATE TABLE Orders (

    Onum INT NOT NULL,
    AMT FLOAT NOT NULL,
    Odate DATE NOT NULL,
    Cnum INT NOT NULL,
    Snum INT NOT NULL,
    CONSTRAINT PK_Orders_Onum PRIMARY KEY(Onum),
    CONSTRAINT FK_Orders_Cnum FOREIGN KEY(Cnum) REFERENCES Customers (Cnum),
    CONSTRAINT FK_Orders_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Orders VALUES
    (3001,18.69,'03-OCT-94',2004,1007),
    (3003,767.19,'03-OCT-94',2001,1001),
    (3002,1900.10,'03-OCT-94',2007,1004),
    (3005,5160.45,'03-OCT-94',2003,1002),
    (3006,1098.16,'04-OCT-94',2004,1007),
    (3009,1713.23,'04-OCT-94',2002,1003),
    (3007,75.75,'05-OCT-94',2004,1002),
    (3008,4723.00,'05-OCT-94',2006,1001),
    (30010,1309.95,'06-OCT-94',2004,1002),
    (30011,9891.88,'06-OCT-94',2006,1001).

SELECT Odate, COUNT(Onum) AS 'Total No of Orders'
FROM Orders
GROUP BY Odate
ORDER BY COUNT(Onum) DESC.


(30.)  All combinations of salespeople and customers who shared a city. (i.e., same city)

CREATE TABLE Salespeople (

    Snum INT NOT NULL PRIMARY KEY,
    Sname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Comm FLOAT
);

INSERT INTO Salespeople VALUES
    (1001,'Peel','London',0.12),
    (1002,'Serres','San Jose',0.13),
    (1004,'Motika','London',0.11),
    (1007,'Rafkin','Barcelona',0.15),
    (1003,'Axelrod','New york',0.1).

CREATE TABLE Customers (

    Cnum INT NOT NULL,
    Cname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Rating INT,
    Snum INT NOT NULL,
    CONSTRAINT PK_Customers_Cnum PRIMARY KEY(Cnum),
    CONSTRAINT FK_Customers_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Customers VALUES 
    (2001,'Hoffman','London',100,1001),
    (2002,'Giovanne','Rome',200,1003),
    (2003,'Liu','San Jose',300,1002),
    (2004,'Grass','Brelin',100,1002),
    (2006,'Clemens','London',300,1007),
    (2007,'Pereira','Rome',100,1004).

SELECT Sname, Cname, S.City AS City
FROM SalesPeople AS S, Customers AS C
WHERE S.City = C.City;


(31.)  Name of all customers matched with the salespeople serving them.

CREATE TABLE Salespeople (

    Snum INT NOT NULL PRIMARY KEY,
    Sname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Comm FLOAT
);

INSERT INTO Salespeople VALUES
    (1001,'Peel','London',0.12),
    (1002,'Serres','San Jose',0.13),
    (1004,'Motika','London',0.11),
    (1007,'Rafkin','Barcelona',0.15),
    (1003,'Axelrod','New york',0.1).

CREATE TABLE Customers (

    Cnum INT NOT NULL,
    Cname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Rating INT,
    Snum INT NOT NULL,
    CONSTRAINT PK_Customers_Cnum PRIMARY KEY(Cnum),
    CONSTRAINT FK_Customers_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Customers VALUES 
    (2001,'Hoffman','London',100,1001),
    (2002,'Giovanne','Rome',200,1003),
    (2003,'Liu','San Jose',300,1002),
    (2004,'Grass','Brelin',100,1002),
    (2006,'Clemens','London',300,1007),
    (2007,'Pereira','Rome',100,1004).

SELECT Cname, Sname 
FROM Customers AS C, SalesPeople AS S
WHERE C.Snum = S.Snum;


(32.)  List each order number followed by the name of the customer who made the order.

CREATE TABLE Customers (

    Cnum INT NOT NULL,
    Cname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Rating INT,
    Snum INT NOT NULL,
    CONSTRAINT PK_Customers_Cnum PRIMARY KEY(Cnum),
    CONSTRAINT FK_Customers_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Customers VALUES 
    (2001,'Hoffman','London',100,1001),
    (2002,'Giovanne','Rome',200,1003),
    (2003,'Liu','San Jose',300,1002),
    (2004,'Grass','Brelin',100,1002),
    (2006,'Clemens','London',300,1007),
    (2007,'Pereira','Rome',100,1004).

CREATE TABLE Orders (

    Onum INT NOT NULL,
    AMT FLOAT NOT NULL,
    Odate DATE NOT NULL,
    Cnum INT NOT NULL,
    Snum INT NOT NULL,
    CONSTRAINT PK_Orders_Onum PRIMARY KEY(Onum),
    CONSTRAINT FK_Orders_Cnum FOREIGN KEY(Cnum) REFERENCES Customers (Cnum),
    CONSTRAINT FK_Orders_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Orders VALUES
    (3001,18.69,'03-OCT-94',2004,1007),
    (3003,767.19,'03-OCT-94',2001,1001),
    (3002,1900.10,'03-OCT-94',2007,1004),
    (3005,5160.45,'03-OCT-94',2003,1002),
    (3006,1098.16,'04-OCT-94',2004,1007),
    (3009,1713.23,'04-OCT-94',2002,1003),
    (3007,75.75,'05-OCT-94',2004,1002),
    (3008,4723.00,'05-OCT-94',2006,1001),
    (30010,1309.95,'06-OCT-94',2004,1002),
    (30011,9891.88,'06-OCT-94',2006,1001).

SELECT Onum, Cname
FROM Customers AS C, Orders AS O
WHERE O.Cnum = C.Cnum;


(33.)  Names of salesperson and customer for each order after the order number.

CREATE TABLE Orders (

    Onum INT NOT NULL,
    AMT FLOAT NOT NULL,
    Odate DATE NOT NULL,
    Cnum INT NOT NULL,
    Snum INT NOT NULL,
    CONSTRAINT PK_Orders_Onum PRIMARY KEY(Onum),
    CONSTRAINT FK_Orders_Cnum FOREIGN KEY(Cnum) REFERENCES Customers (Cnum),
    CONSTRAINT FK_Orders_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Orders VALUES
    (3001,18.69,'03-OCT-94',2004,1007),
    (3003,767.19,'03-OCT-94',2001,1001),
    (3002,1900.10,'03-OCT-94',2007,1004),
    (3005,5160.45,'03-OCT-94',2003,1002),
    (3006,1098.16,'04-OCT-94',2004,1007),
    (3009,1713.23,'04-OCT-94',2002,1003),
    (3007,75.75,'05-OCT-94',2004,1002),
    (3008,4723.00,'05-OCT-94',2006,1001),
    (30010,1309.95,'06-OCT-94',2004,1002),
    (30011,9891.88,'06-OCT-94',2006,1001).

CREATE TABLE Customers (

    Cnum INT NOT NULL,
    Cname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Rating INT,
    Snum INT NOT NULL,
    CONSTRAINT PK_Customers_Cnum PRIMARY KEY(Cnum),
    CONSTRAINT FK_Customers_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Customers VALUES 
    (2001,'Hoffman','London',100,1001),
    (2002,'Giovanne','Rome',200,1003),
    (2003,'Liu','San Jose',300,1002),
    (2004,'Grass','Brelin',100,1002),
    (2006,'Clemens','London',300,1007),
    (2007,'Pereira','Rome',100,1004).

CREATE TABLE Salespeople (

    Snum INT NOT NULL PRIMARY KEY,
    Sname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Comm FLOAT
);

INSERT INTO Salespeople VALUES
    (1001,'Peel','London',0.12),
    (1002,'Serres','San Jose',0.13),
    (1004,'Motika','London',0.11),
    (1007,'Rafkin','Barcelona',0.15),
    (1003,'Axelrod','New york',0.1).

SELECT Onum, Sname, Cname
FROM Orders AS O, Customers AS C, SalesPeople AS S
WHERE O.Cnum = C.Cnum and O.Snum = S.Snum;


(34.) Produce all customer serviced by salespeople with a commission above 12%.

CREATE TABLE Customers (

    Cnum INT NOT NULL,
    Cname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Rating INT,
    Snum INT NOT NULL,
    CONSTRAINT PK_Customers_Cnum PRIMARY KEY(Cnum),
    CONSTRAINT FK_Customers_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Customers VALUES 
    (2001,'Hoffman','London',100,1001),
    (2002,'Giovanne','Rome',200,1003),
    (2003,'Liu','San Jose',300,1002),
    (2004,'Grass','Brelin',100,1002),
    (2006,'Clemens','London',300,1007),
    (2007,'Pereira','Rome',100,1004).

CREATE TABLE Salespeople (

    Snum INT NOT NULL PRIMARY KEY,
    Sname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Comm FLOAT
);

INSERT INTO Salespeople VALUES
    (1001,'Peel','London',0.12),
    (1002,'Serres','San Jose',0.13),
    (1004,'Motika','London',0.11),
    (1007,'Rafkin','Barcelona',0.15),
    (1003,'Axelrod','New york',0.1).

SELECT Cname, Sname, Comm
FROM Customers AS C, SalesPeople AS S
WHERE Comm > 0.12 AND C.Snum = S.Snum;


(35.)  Calculate the amount of the salesperson’s commission on each order with a rating above 100.

CREATE TABLE Customers (

    Cnum INT NOT NULL,
    Cname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Rating INT,
    Snum INT NOT NULL,
    CONSTRAINT PK_Customers_Cnum PRIMARY KEY(Cnum),
    CONSTRAINT FK_Customers_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Customers VALUES 
    (2001,'Hoffman','London',100,1001),
    (2002,'Giovanne','Rome',200,1003),
    (2003,'Liu','San Jose',300,1002),
    (2004,'Grass','Brelin',100,1002),
    (2006,'Clemens','London',300,1007),
    (2007,'Pereira','Rome',100,1004).

CREATE TABLE Salespeople (

    Snum INT NOT NULL PRIMARY KEY,
    Sname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Comm FLOAT
);

INSERT INTO Salespeople VALUES
    (1001,'Peel','London',0.12),
    (1002,'Serres','San Jose',0.13),
    (1004,'Motika','London',0.11),
    (1007,'Rafkin','Barcelona',0.15),
    (1003,'Axelrod','New york',0.1).

CREATE TABLE Orders (

    Onum INT NOT NULL,
    AMT FLOAT NOT NULL,
    Odate DATE NOT NULL,
    Cnum INT NOT NULL,
    Snum INT NOT NULL,
    CONSTRAINT PK_Orders_Onum PRIMARY KEY(Onum),
    CONSTRAINT FK_Orders_Cnum FOREIGN KEY(Cnum) REFERENCES Customers (Cnum),
    CONSTRAINT FK_Orders_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Orders VALUES
    (3001,18.69,'03-OCT-94',2004,1007),
    (3003,767.19,'03-OCT-94',2001,1001),
    (3002,1900.10,'03-OCT-94',2007,1004),
    (3005,5160.45,'03-OCT-94',2003,1002),
    (3006,1098.16,'04-OCT-94',2004,1007),
    (3009,1713.23,'04-OCT-94',2002,1003),
    (3007,75.75,'05-OCT-94',2004,1002),
    (3008,4723.00,'05-OCT-94',2006,1001),
    (30010,1309.95,'06-OCT-94',2004,1002),
    (30011,9891.88,'06-OCT-94',2006,1001).

SELECT Sname, AMT*Comm, Rating
FROM Customers AS C, Salespeople AS S, Orders AS O
WHERE Rating > 100 AND 
        S.Snum = C.Snum AND 
        S.Snum = O.Snum AND 
        O.Cnum = C.Cnum;


(36.)  Find all pairs of customers having the same rating.

CREATE TABLE Customers (

    Cnum INT NOT NULL,
    Cname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Rating INT,
    Snum INT NOT NULL,
    CONSTRAINT PK_Customers_Cnum PRIMARY KEY(Cnum),
    CONSTRAINT FK_Customers_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Customers VALUES 
    (2001,'Hoffman','London',100,1001),
    (2002,'Giovanne','Rome',200,1003),
    (2003,'Liu','San Jose',300,1002),
    (2004,'Grass','Brelin',100,1002),
    (2006,'Clemens','London',300,1007),
    (2007,'Pereira','Rome',100,1004).

SELECT a.Cname, b.Cname, a.Rating
FROM Customers a, Customers b
WHERE a.Rating = b.Rating and a.Cnum != b.Cnum;


(37.)  Policy is to assign three salespersons to each customer. Display all such combinations.

CREATE TABLE Customers (

    Cnum INT NOT NULL,
    Cname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Rating INT,
    Snum INT NOT NULL,
    CONSTRAINT PK_Customers_Cnum PRIMARY KEY(Cnum),
    CONSTRAINT FK_Customers_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Customers VALUES 
    (2001,'Hoffman','London',100,1001),
    (2002,'Giovanne','Rome',200,1003),
    (2003,'Liu','San Jose',300,1002),
    (2004,'Grass','Brelin',100,1002),
    (2006,'Clemens','London',300,1007),
    (2007,'Pereira','Rome',100,1004).

Select Cname, Sname
FROM SalesPeople, Customers
WHERE Sname IN (SELECT Sname FROM salespeople WHERE rownum <= 3)
ORDER BY Cname.






(38.)  Display all customers located in cities where salesman serves has customer.

CREATE TABLE Salespeople (

    Snum INT NOT NULL PRIMARY KEY,
    Sname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Comm FLOAT
);

INSERT INTO Salespeople VALUES
    (1001,'Peel','London',0.12),
    (1002,'Serres','San Jose',0.13),
    (1004,'Motika','London',0.11),
    (1007,'Rafkin','Barcelona',0.15),
    (1003,'Axelrod','New york',0.1).

CREATE TABLE Customers (

    Cnum INT NOT NULL,
    Cname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Rating INT,
    Snum INT NOT NULL,
    CONSTRAINT PK_Customers_Cnum PRIMARY KEY(Cnum),
    CONSTRAINT FK_Customers_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Customers VALUES 
    (2001,'Hoffman','London',100,1001),
    (2002,'Giovanne','Rome',200,1003),
    (2003,'Liu','San Jose',300,1002),
    (2004,'Grass','Brelin',100,1002),
    (2006,'Clemens','London',300,1007),
    (2007,'Pereira','Rome',100,1004).

SELECT Cname
FROM Customers
WHERE City IN (SELECT City FROM Customers AS C, Orders AS O
                WHERE C.Cnum = O.Cnum AND 
                    O.Snum IN ( SELECT Snum FROM Salespeople 
                                WHERE Sname = 'Serres')).

(39.)  Find all pairs of customers served by single salesperson.

CREATE TABLE Customers (

    Cnum INT NOT NULL,
    Cname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Rating INT,
    Snum INT NOT NULL,
    CONSTRAINT PK_Customers_Cnum PRIMARY KEY(Cnum),
    CONSTRAINT FK_Customers_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Customers VALUES 
    (2001,'Hoffman','London',100,1001),
    (2002,'Giovanne','Rome',200,1003),
    (2003,'Liu','San Jose',300,1002),
    (2004,'Grass','Brelin',100,1002),
    (2006,'Clemens','London',300,1007),
    (2007,'Pereira','Rome',100,1004).

CREATE TABLE Salespeople (

    Snum INT NOT NULL PRIMARY KEY,
    Sname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Comm FLOAT
);

INSERT INTO Salespeople VALUES
    (1001,'Peel','London',0.12),
    (1002,'Serres','San Jose',0.13),
    (1004,'Motika','London',0.11),
    (1007,'Rafkin','Barcelona',0.15),
    (1003,'Axelrod','New york',0.1).

SELECT DISTINCT a.Cname
FROM Customers a, Customers b
WHERE a.Snum = b.Snum and a.Cnum != b.Cnum;


(40.)  Produce all pairs of salespeople which are living in the same city. Exclude combinations of salespeople with themselves as well as duplicates with the order reversed.

CREATE TABLE Salespeople (

    Snum INT NOT NULL PRIMARY KEY,
    Sname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Comm FLOAT
);

INSERT INTO Salespeople VALUES
    (1001,'Peel','London',0.12),
    (1002,'Serres','San Jose',0.13),
    (1004,'Motika','London',0.11),
    (1007,'Rafkin','Barcelona',0.15),
    (1003,'Axelrod','New york',0.1).

SELECT a.Sname, b.Sname
FROM SalesPeople a, SalesPeople b
WHERE a.Snum > b.Snum AND a.City = b.City;

(41.)  Produce names and cities of all customers with the same rating as Hoffman.

CREATE TABLE Customers (

    Cnum INT NOT NULL,
    Cname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Rating INT,
    Snum INT NOT NULL,
    CONSTRAINT PK_Customers_Cnum PRIMARY KEY(Cnum),
    CONSTRAINT FK_Customers_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Customers VALUES 
    (2001,'Hoffman','London',100,1001),
    (2002,'Giovanne','Rome',200,1003),
    (2003,'Liu','San Jose',300,1002),
    (2004,'Grass','Brelin',100,1002),
    (2006,'Clemens','London',300,1007),
    (2007,'Pereira','Rome',100,1004).

SELECT a.Sname, b.Sname
FROM SalesPeople a, SalesPeople b
WHERE a.Snum > b.Snum AND a.City = b.City;


(42.)  Extract all the orders of Motika.

CREATE TABLE Orders (

    Onum INT NOT NULL,
    AMT FLOAT NOT NULL,
    Odate DATE NOT NULL,
    Cnum INT NOT NULL,
    Snum INT NOT NULL,
    CONSTRAINT PK_Orders_Onum PRIMARY KEY(Onum),
    CONSTRAINT FK_Orders_Cnum FOREIGN KEY(Cnum) REFERENCES Customers (Cnum),
    CONSTRAINT FK_Orders_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Orders VALUES
    (3001,18.69,'03-OCT-94',2004,1007),
    (3003,767.19,'03-OCT-94',2001,1001),
    (3002,1900.10,'03-OCT-94',2007,1004),
    (3005,5160.45,'03-OCT-94',2003,1002),
    (3006,1098.16,'04-OCT-94',2004,1007),
    (3009,1713.23,'04-OCT-94',2002,1003),
    (3007,75.75,'05-OCT-94',2004,1002),
    (3008,4723.00,'05-OCT-94',2006,1001),
    (30010,1309.95,'06-OCT-94',2004,1002),
    (30011,9891.88,'06-OCT-94',2006,1001).


CREATE TABLE Salespeople (

    Snum INT NOT NULL PRIMARY KEY,
    Sname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Comm FLOAT
);

INSERT INTO Salespeople VALUES
    (1001,'Peel','London',0.12),
    (1002,'Serres','San Jose',0.13),
    (1004,'Motika','London',0.11),
    (1007,'Rafkin','Barcelona',0.15),
    (1003,'Axelrod','New york',0.1).

SELECT Onum
FROM Orders
WHERE Snum = (SELECT Snum FROM Salespeople WHERE Sname = 'Motika');

(43.)  All orders credited to the same salesperson who services Hoffman.

CREATE TABLE Orders (

    Onum INT NOT NULL,
    AMT FLOAT NOT NULL,
    Odate DATE NOT NULL,
    Cnum INT NOT NULL,
    Snum INT NOT NULL,
    CONSTRAINT PK_Orders_Onum PRIMARY KEY(Onum),
    CONSTRAINT FK_Orders_Cnum FOREIGN KEY(Cnum) REFERENCES Customers (Cnum),
    CONSTRAINT FK_Orders_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Orders VALUES
    (3001,18.69,'03-OCT-94',2004,1007),
    (3003,767.19,'03-OCT-94',2001,1001),
    (3002,1900.10,'03-OCT-94',2007,1004),
    (3005,5160.45,'03-OCT-94',2003,1002),
    (3006,1098.16,'04-OCT-94',2004,1007),
    (3009,1713.23,'04-OCT-94',2002,1003),
    (3007,75.75,'05-OCT-94',2004,1002),
    (3008,4723.00,'05-OCT-94',2006,1001),
    (30010,1309.95,'06-OCT-94',2004,1002),
    (30011,9891.88,'06-OCT-94',2006,1001).

CREATE TABLE Salespeople (

    Snum INT NOT NULL PRIMARY KEY,
    Sname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Comm FLOAT
);

INSERT INTO Salespeople VALUES
    (1001,'Peel','London',0.12),
    (1002,'Serres','San Jose',0.13),
    (1004,'Motika','London',0.11),
    (1007,'Rafkin','Barcelona',0.15),
    (1003,'Axelrod','New york',0.1).

SELECT Onum, sname, Cname, AMT
from Orders AS O, Salespeople AS S, Customers C
where O.Snum = S.Snum AND O.Cnum = C.Cnum AND
          O.Snum = ( SELECT Snum FROM Orders
                        WHERE Cnum = (SELECT Cnum FROM Customers
                                        WHERE Cname = 'Hoffman')).


(44.)  All orders that are greater than the average for Oct 4.

CREATE TABLE Orders (

    Onum INT NOT NULL,
    AMT FLOAT NOT NULL,
    Odate DATE NOT NULL,
    Cnum INT NOT NULL,
    Snum INT NOT NULL,
    CONSTRAINT PK_Orders_Onum PRIMARY KEY(Onum),
    CONSTRAINT FK_Orders_Cnum FOREIGN KEY(Cnum) REFERENCES Customers (Cnum),
    CONSTRAINT FK_Orders_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Orders VALUES
    (3001,18.69,'03-OCT-94',2004,1007),
    (3003,767.19,'03-OCT-94',2001,1001),
    (3002,1900.10,'03-OCT-94',2007,1004),
    (3005,5160.45,'03-OCT-94',2003,1002),
    (3006,1098.16,'04-OCT-94',2004,1007),
    (3009,1713.23,'04-OCT-94',2002,1003),
    (3007,75.75,'05-OCT-94',2004,1002),
    (3008,4723.00,'05-OCT-94',2006,1001),
    (30010,1309.95,'06-OCT-94',2004,1002),
    (30011,9891.88,'06-OCT-94',2006,1001).

SELECT *
FROM Orders
WHERE AMT > (SELECT AVG(AMT) FROM Orders
                WHERE Odate = '03-OCT-94').


(45.) Find average commission of salespeople in London.

CREATE TABLE Salespeople (

    Snum INT NOT NULL PRIMARY KEY,
    Sname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Comm FLOAT
);

INSERT INTO Salespeople VALUES
    (1001,'Peel','London',0.12),
    (1002,'Serres','San Jose',0.13),
    (1004,'Motika','London',0.11),
    (1007,'Rafkin','Barcelona',0.15),
    (1003,'Axelrod','New york',0.1).

SELECT AVG(Comm)
FROM Salespeople
WHERE City = 'London’.


(46.)  Find all orders attributed to salespeople servicing customers in London.

CREATE TABLE Orders (

    Onum INT NOT NULL,
    AMT FLOAT NOT NULL,
    Odate DATE NOT NULL,
    Cnum INT NOT NULL,
    Snum INT NOT NULL,
    CONSTRAINT PK_Orders_Onum PRIMARY KEY(Onum),
    CONSTRAINT FK_Orders_Cnum FOREIGN KEY(Cnum) REFERENCES Customers (Cnum),
    CONSTRAINT FK_Orders_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Orders VALUES
    (3001,18.69,'03-OCT-94',2004,1007),
    (3003,767.19,'03-OCT-94',2001,1001),
    (3002,1900.10,'03-OCT-94',2007,1004),
    (3005,5160.45,'03-OCT-94',2003,1002),
    (3006,1098.16,'04-OCT-94',2004,1007),
    (3009,1713.23,'04-OCT-94',2002,1003),
    (3007,75.75,'05-OCT-94',2004,1002),
    (3008,4723.00,'05-OCT-94',2006,1001),
    (30010,1309.95,'06-OCT-94',2004,1002),
    (30011,9891.88,'06-OCT-94',2006,1001).

SELECT Snum, Cnum
FROM Orders
WHERE Cnum IN (SELECT Cnum FROM Customers WHERE City = 'London').


(47.)  Extract commissions of all salespeople servicing customers in London.

CREATE TABLE Salespeople (

    Snum INT NOT NULL PRIMARY KEY,
    Sname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Comm FLOAT
);

INSERT INTO Salespeople VALUES
    (1001,'Peel','London',0.12),
    (1002,'Serres','San Jose',0.13),
    (1004,'Motika','London',0.11),
    (1007,'Rafkin','Barcelona',0.15),
    (1003,'Axelrod','New york',0.1).

SELECT Comm
FROM Salespeople
WHERE Snum IN (SELECT Snum FROM Customers WHERE City = 'London').


(48.)  Find all customers whose cnum is 1000 above the snum of serves.

CREATE TABLE Customers (

    Cnum INT NOT NULL,
    Cname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Rating INT,
    Snum INT NOT NULL,
    CONSTRAINT PK_Customers_Cnum PRIMARY KEY(Cnum),
    CONSTRAINT FK_Customers_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Customers VALUES 
    (2001,'Hoffman','London',100,1001),
    (2002,'Giovanne','Rome',200,1003),
    (2003,'Liu','San Jose',300,1002),
    (2004,'Grass','Brelin',100,1002),
    (2006,'Clemens','London',300,1007),
    (2007,'Pereira','Rome',100,1004).

SELECT Cnum, Cname from Customers
where Cnum > (SELECT Snum + 1000
                FROM Salespeople
                WHERE Sname = 'Serves').


(49.)  Count the customers with rating above San Jose’s average.

CREATE TABLE Customers (

    Cnum INT NOT NULL,
    Cname VARCHAR (50) NOT NULL,
    City VARCHAR (50),
    Rating INT,
    Snum INT NOT NULL,
    CONSTRAINT PK_Customers_Cnum PRIMARY KEY(Cnum),
    CONSTRAINT FK_Customers_Snum FOREIGN KEY(Snum) REFERENCES Salespeople (Snum)
);

INSERT INTO Customers
VALUES 
    (2001,'Hoffman','London',100,1001),
    (2002,'Giovanne','Rome',200,1003),
    (2003,'Liu','San Jose',300,1002),
    (2004,'Grass','Brelin',100,1002),
    (2006,'Clemens','London',300,1007),
    (2007,'Pereira','Rome',100,1004).


SELECT cnum, rating from Customers
Where rating> (SELECT avg(rating)
FROM Customers
Where city=’San Jose’).









