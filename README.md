# w7d1-learn-sql

Questions:

**1.  How many users are there?**

50
```
select count(*) from users;
```
**2.  What are the 5 most expensive items?**


Small Cotton Gloves  9984      
Small Wooden Comput  9859      
Awesome Granite Pan  9790      
Sleek Wooden Hat     9390      
Ergonomic Steel Car  9341 

```
select title, price from items order by price DESC limit 5;
```


**3.  What's the cheapest book? (Does that change for "category is exactly 'book'" versus "category contains 'book'"?)**
 

Books       Ergonomic Granite Chair  1496 
```
select category, title, price from items where category like '%book%' order by price limit 1;
```

**4.  Who lives at "6439 Zetta Hills, Willmouth, WY"? Do they have another address?**

Corrine Little

yes, 54369 Wolff Forg, Lake Bryon, CA 31587
```
select user_id from addresses where street like '%Zetta%'; //40
select * from addresses where user_id like '40';  
select addresses.user_id, users.first_name, users.last_name from addresses inner join users on addresses.user_id=users.id where street like '%Zetta%';
```

**5.  Correct Virginie Mitchell's address to "New York, NY, 10108".**


```
 select id from users where last_name='Mitchell';
 update addresses set city='New York', zip='10108' where id=41;
```

**6. How much would it cost to buy one of each tool?**

46477 
```
select sum(price) from items where category like '%tools%';
```

**7. How many total items did we sell?**

2125  
```
select sum(quantity) from orders;
```

**8. How much was spent on books?**

420566     

```
select sum(items.price*orders.quantity) from items inner join orders on items.id=orders.item_id where category='Books';
```

**9. Simulate buying an item by inserting a User for yourself and an Order for that User.**
```
insert into users values(51, 'Young Mi', 'Kim','ymkim23@gmail.com');
insert into orders(user_id, item_id, quantity, created_at) values(51, 97, 1, datetime());
```

