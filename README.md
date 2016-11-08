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

other address is 54369 Wolff Forg, Lake Bryon, CA 31587
```
select user_id from addresses where street like '%Zetta%'; //40
select * from addresses where user_id like '40';  
select addresses.user_id, users.first_name, users.last_name from addresses inner join users on addresses.user_id=users.id where street like '%Zetta%';
```

**5.  Correct Virginie Mitchell's address to "New York, NY, 10108".**

I looked up Virginie's id by: select users.id, users.first_name, users.last_name from users where first_name='Virginie'; To correct her address I did: Command - update addresses set city='New York', zip='10108' where id=41;

A.) I Found out the id for virginie first then updated her address. Command Used: select users.id, users.first_name, users.last_name from users where first_name like '%virginie%'; Command Used: select users.id, users.first_name, users.last_name from users inner join addresses on users.id=addresses.user_id; Command Used: update addresses set city='New York', state='NY', zip='10108' where addresses.id=41;

 select id from users where last_name='Mitchell';


**6. How much would it cost to buy one of each tool?**

46477 
```
select sum(price) from items where category like '%tools%';
```

**7. How many total items did we sell?**



**8. How much was spent on books?**



**9. Simulate buying an item by inserting a User for yourself and an Order for that User.**
insert

