
1. Количество клиентов из Германии 11;

```sql
SELECT count(*) FROM Customers
where Country like 'Germany'
```
2. Имена 14 клиентов начинаются с 'e'

```sql
SELECT count(CustomerName) FROM Customers
where CustomerName like '%e'
```

3. Вставка моего имени в список

```sql
insert into Customers (CustomerID,CustomerName,ContactName,Address,City,PostalCode,Country)
values (92,'Kseniya Drozhzhina','Kseniya Drozhzhina','Solnechnaiya Str.15','More','123456','Russia')
```
![image 1](3_insert.png)
![image 2](3_insert1.png)

4. Изменение моего имени в таблице

```sql
update Customers set CustomerName = 'Drozhzhina Kseniya'
where CustomerID = 92
```
![image 3](4_rename.png)

5. Удаление всех клиентов из города Nantes

```sql
delete FROM Customers 
where City = 'Nantes'
```
![image 4](5_Nantes.png)

6. Номера заказов, оформленных для клиентов работником с именем Steven

```sql
SELECT OrderID
FROM Orders, FirstName
INNER JOIN Employees ON Employees.EmployeeID = Orders.EmployeeID
where FirstName='Steven'
```
![image 5](6_Orders_Steven.png)

