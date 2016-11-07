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



**5.  Correct Virginie Mitchell's address to "New York, NY, 10108".**



**6. How much would it cost to buy one of each tool?**



**7. How many total items did we sell?**



**8. How much was spent on books?**



**9. Simulate buying an item by inserting a User for yourself and an Order for that User.**

