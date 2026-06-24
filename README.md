# retail_store_analysis
CREATE DATABASE retail_store_db;
USE retail_store_db;
show tables ;
create table sales (
sale_id INT,
     customer_name VARCHAR(50),
    gender VARCHAR(10),
    age INT,
	city VARCHAR(30),
	category VARCHAR(30),
	product_name VARCHAR(50),
    payment_mode VARCHAR(20),
	quantity INT,
    price DECIMAL(10,2),
    rating DECIMAL(2,1),
     order_date DATE
    );
    insert into sales values
(1,'Akash','Male',24,'Pune','Electronics','Laptop','UPI',1,55000,4.8,'2026-01-10'), 
(2,'Rahul','Male',26,'Mumbai','Fashion','Shirt','Card',2,2500,4.2,'2026-01-11'), 
(3,'Sneha','Female',23,'Delhi','Beauty','Lipstick','UPI',3,1500,4.5,'2026-01-12'), 
(4,'Priya','Female',25,'Pune','Electronics','Mobile','Card',1,25000,4.7,'2026-01-13'), 
(5,'Aman','Male',28,'Indore','Sports','Cricket Bat','Cash',1,3000,4.1,'2026-01-14'), 
(6,'Rohit','Male',27,'Mumbai','Electronics','Headphones','UPI',2,4000,4.3,'2026-01-15'), 
(7,'Riya','Female',24,'Delhi','Fashion','Jeans','Card',1,2200,4.4,'2026-01-16'), 
(8,'Karan','Male',29,'Pune','Sports','Football','Cash',2,1800,4.0,'2026-01-17'), 
(9,'Neha','Female',22,'Bhopal','Beauty','Face Wash','UPI',4,800,4.6,'2026-01-18'), 
(10,'Vikas','Male',31,'Jaipur','Electronics','Tablet','Card',1,18000,4.5,'2026-01-19'), 
(11,'Pooja','Female',27,'Pune','Fashion','Kurti','UPI',2,1700,4.3,'2026-01-20'), 
(12,'Arjun','Male',30,'Delhi','Electronics','Smart Watch','Card',1,9000,4.6,'2026-01-21'), 
(13,'Anjali','Female',26,'Mumbai','Beauty','Perfume','Cash',1,3500,4.2,'2026-01-22'), 
(14,'Yash','Male',25,'Indore','Sports','Badminton Kit','UPI',1,2800,4.4,'2026-01-23'), 
(15,'Meera','Female',28,'Pune','Electronics','Camera','Card',1,45000,4.9,'2026-01-24'), 
(16,'Sahil','Male',24,'Bhopal','Fashion','Jacket','UPI',1,3200,4.1,'2026-01-25'), 
(17,'Nikita','Female',29,'Jaipur','Beauty','Moisturizer','Card',2,1200,4.7,'2026-01-26'), 
(18,'Harsh','Male',32,'Delhi','Sports','Gym Gloves','Cash',3,900,4.0,'2026-01-27'), 
(19,'Simran','Female',23,'Mumbai','Electronics','Earbuds','UPI',2,2500,4.5,'2026-01-28'), 
(20,'Deepak','Male',27,'Pune','Fashion','T-Shirt','Card',3,1800,4.2,'2026-01-29')
;

	Q 1 : Display all records from the sales table. 
select * from sales;
<img width="595" height="203" alt="Screenshot 2026-06-24 175106" src="https://github.com/user-attachments/assets/1edb41c6-99b9-460a-98e2-13052952549e" />

 Q2 :  Display only customer names. 
select customer_name from sales;
<img width="90" height="183" alt="Screenshot 2026-06-24 175650" src="https://github.com/user-attachments/assets/a18f65d2-6ef9-42e8-a0d2-2b54ab200645" />

Q3 :  Display customer names and cities. 
select customer_name , city from sales;
<img width="129" height="185" alt="Screenshot 2026-06-24 175808" src="https://github.com/user-attachments/assets/f4c102cd-3b40-40f8-bf9b-7e95719ed4dc" />

Q4 :  Display product names and prices.
select product_name ,price from sales;
<img width="132" height="182" alt="Screenshot 2026-06-24 175937" src="https://github.com/user-attachments/assets/70c15494-59e5-45a9-a770-28220851bd06" />

Q5 :  Display all unique cities. 
select distinct city from sales;
<img width="60" height="94" alt="Screenshot 2026-06-24 180652" src="https://github.com/user-attachments/assets/4ecf1a1c-c5d7-472c-ac74-40522e2dd03e" />

Q 6 : Display all unique categories.
select distinct category from sales;
<img width="67" height="68" alt="Screenshot 2026-06-24 180813" src="https://github.com/user-attachments/assets/b74c7f5b-00d5-43b1-b8b6-2f1520ed37fb" />

Q 7 : Display all unique payment methods.
select distinct payment_mode from sales;
<img width="88" height="52" alt="Screenshot 2026-06-24 180909" src="https://github.com/user-attachments/assets/eb323302-7ac3-430e-8713-d6184ead0c9e" />

Q 8 :  Display all male customers. 
select * from sales where gender="male";
<img width="596" height="161" alt="Screenshot 2026-06-24 181058" src="https://github.com/user-attachments/assets/54b534b4-1a45-4a4b-95c9-89a21b19c9d7" />

 Q9 :  Display all female customers. 
select * from sales where gender="female";
<img width="593" height="133" alt="Screenshot 2026-06-24 181205" src="https://github.com/user-attachments/assets/4a7a33c2-0cc8-457c-8294-ed9fd01585fd" />

10 :  Display customer name and rating.

select customer_name, rating from sales;
<img width="122" height="232" alt="Screenshot 2026-06-24 181846" src="https://github.com/user-attachments/assets/142260cc-b5ac-4f4a-b142-d3df571f002f" /> 
<img width="122" height="41" alt="Screenshot 2026-06-24 181930" src="https://github.com/user-attachments/assets/dc077576-bf20-404a-8780-772a67488500" />



 11 : Display all customers from Pune. 
select * from sales where city ="pune";
<img width="583" height="92" alt="Screenshot 2026-06-24 182119" src="https://github.com/user-attachments/assets/00c49ca4-70c0-4f8a-93b8-0f934c7913d3" />

12 :  Display all customers from Mumbai. 
select * from sales where city ="mumbai";
<img width="586" height="67" alt="Screenshot 2026-06-24 182407" src="https://github.com/user-attachments/assets/68c1c816-533f-47f5-a2bb-3a2c200c9122" />

13 :  Display all Electronics products. 
select * from sales where category ="electronics";
<img width="597" height="106" alt="Screenshot 2026-06-24 182519" src="https://github.com/user-attachments/assets/4aec5080-49af-4fc6-b7bc-e8a5aa071558" />

14 : Display all Fashion products. 
select * from sales where category ="fashion";
<img width="581" height="80" alt="Screenshot 2026-06-24 182611" src="https://github.com/user-attachments/assets/47bf84ec-aa4a-4d19-97b6-684d37718136" />

15 :  Display all Sports products. 
select * from sales where category ="sports";
<img width="586" height="65" alt="Screenshot 2026-06-24 183124" src="https://github.com/user-attachments/assets/e8dc239b-bc42-48ff-b40b-b18bfc41aa48" />

Q 16 :  Display products with price greater than 5000. 
select *from sales where price >5000;
<img width="590" height="82" alt="Screenshot 2026-06-24 183223" src="https://github.com/user-attachments/assets/e398c39c-32de-48e4-b098-ccbf4570eeca" />

Q 17 :  Display products with price less than 5000.
select * from sales where price <5000;
<img width="590" height="211" alt="Screenshot 2026-06-24 183407" src="https://github.com/user-attachments/assets/673f95b3-e3ed-4f3e-9112-ea31e75ba01a" />

18 : Display customers whose age is greater than 25.
select * from sales where age <25;
<img width="595" height="93" alt="Screenshot 2026-06-24 183517" src="https://github.com/user-attachments/assets/55f68acd-4ed1-4c77-8f4f-efe63812a740" />

 Q 19 :  Display customers whose age is less than 25. 
select * from sales where age >25;
<img width="593" height="170" alt="Screenshot 2026-06-24 183622" src="https://github.com/user-attachments/assets/fdd1c6b5-6c91-4f24-afae-b337093b139e" />

Q 20 : Display products with rating greater than 4.5. 
select * from sales where rating >4.5;
<img width="591" height="96" alt="Screenshot 2026-06-24 184329" src="https://github.com/user-attachments/assets/c25dd8ab-d4ab-4521-b615-6ead5c19a265" />

 Q 21 : Display all UPI transactions.
select * from sales where payment_mode ="upi";
<img width="590" height="119" alt="Screenshot 2026-06-24 184422" src="https://github.com/user-attachments/assets/c1597e80-f05c-410f-8ed2-1a54095466c8" />

Q 22 :  Display all Card transactions. 
select * from sales where payment_mode ="card";
<img width="593" height="118" alt="Screenshot 2026-06-24 184519" src="https://github.com/user-attachments/assets/dd1cb90c-bc37-41fa-be8d-c76fdc492b2e" />

Q 23 : Display all Cash transactions. 
select * from sales where payment_mode ="cash";
<img width="581" height="67" alt="Screenshot 2026-06-24 184614" src="https://github.com/user-attachments/assets/f028f4eb-84da-4880-b6f7-209217e1bca6" />

 Q 24 : Display Electronics products from Pune. 
select * from sales where category ="electronics" and city ="pune";
<img width="590" height="53" alt="Screenshot 2026-06-24 185703" src="https://github.com/user-attachments/assets/e17a7df8-bbb3-4b0e-8f4d-b2dff353f875" />

Q 25 :  Display Fashion products from Mumbai.
select * from sales where category ="fashion" and city ="mumbai";
<img width="590" height="29" alt="Screenshot 2026-06-24 185800" src="https://github.com/user-attachments/assets/40eb8dcc-41a5-43f0-a7eb-c6c9ea2cdaa7" />

Q 26 : Display Female customers from Delhi. 
select * from sales where gender ="female" and city ='delhi';
<img width="578" height="44" alt="Screenshot 2026-06-24 185850" src="https://github.com/user-attachments/assets/71cf2ea3-a7c6-4e08-827e-52cd267cbf49" />

Q 27 : Display Male customers from Pune.
select * from sales where gender ="male" and city ="pune";
<img width="584" height="59" alt="Screenshot 2026-06-24 185945" src="https://github.com/user-attachments/assets/819fb26b-0e6c-489c-a750-3c6d521374f9" />

Q 28 :  Display products priced between 2000 and 10000. 
select * from sales where price between 2000 and 10000 ;
<img width="596" height="132" alt="Screenshot 2026-06-24 190036" src="https://github.com/user-attachments/assets/8ccfaaf5-ed90-4847-8284-83206a368927" />












