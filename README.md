# w7d1-learn-sql

Questions:

**1.  How many users are there?**

50
```
select count(*) from users;
```
**2.  What are the 5 most expensive items?**
id          title                category                    description                         price     
----------  -------------------  --------------------------  ----------------------------------  ----------
25          Small Cotton Gloves  Automotive, Shoes & Beauty  Multi-layered modular service-desk  9984      
83          Small Wooden Comput  Health                      Re-engineered fault-tolerant adapt  9859      
100         Awesome Granite Pan  Toys & Books                Upgradable 24/7 access              9790      
40          Sleek Wooden Hat     Music & Baby                Quality-focused heuristic info-med  9390      
60          Ergonomic Steel Car  Books & Outdoors            Enterprise-wide secondary firmware  9341      

```
select * from items order by price DESC limit 5;
```


**3.  What's the cheapest book? (Does that change for "category is exactly 'book'" versus "category contains 'book'"?)**



**4.  Who lives at "6439 Zetta Hills, Willmouth, WY"? Do they have another address?**



**5.  Correct Virginie Mitchell's address to "New York, NY, 10108".**



**6. How much would it cost to buy one of each tool?**



**7. How many total items did we sell?**



**8. How much was spent on books?**



**9. Simulate buying an item by inserting a User for yourself and an Order for that User.**

