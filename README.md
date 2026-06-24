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

Q 29 :  Display customers aged between 24 and 30.
select * from sales where age between 24 and 30 ;
<img width="599" height="209" alt="Screenshot 2026-06-24 190213" src="https://github.com/user-attachments/assets/611c8a04-a7b8-45df-ac7b-de1df8fe2e53" />

Q 30 : Display orders placed after 20 January 2026.
select * from sales where order_date >'2026-01-20';
<img width="596" height="131" alt="Screenshot 2026-06-24 190656" src="https://github.com/user-attachments/assets/1cd6670e-3e08-41d2-ae0b-d69d6ec8f3a5" />


Q 31 :  Sort products by price in ascending order.
select * from sales order by price ASC;
<img width="593" height="177" alt="Screenshot 2026-06-24 191001" src="https://github.com/user-attachments/assets/75624840-2920-4ee9-943c-a2afd17b8bcf" />
<img width="590" height="88" alt="Screenshot 2026-06-24 191036" src="https://github.com/user-attachments/assets/89f8ec64-6019-4d22-af4b-4985444f9ea7" />

 Q 32 :  Sort products by price in descending order.
select * from sales order by price DESC;
<img width="590" height="167" alt="Screenshot 2026-06-24 191352" src="https://github.com/user-attachments/assets/2c84620c-3926-4f49-9161-b90d92a1339e" />
<img width="593" height="103" alt="Screenshot 2026-06-24 191437" src="https://github.com/user-attachments/assets/03480d05-8d16-4dbc-994c-eab529ddf8e2" />

Q 33 :  Sort customers by age in ascending order. 
select * from sales order by age ASC;
<img width="596" height="166" alt="Screenshot 2026-06-24 191700" src="https://github.com/user-attachments/assets/5853e1f9-7571-4c83-8528-30252e933d49" />
<img width="591" height="104" alt="Screenshot 2026-06-24 191736" src="https://github.com/user-attachments/assets/229b31b9-caf3-4067-8b23-62fa2a925b57" />

Q 34 :  Sort customers by age in descending order.
select * from sales order by age DESC;
<img width="593" height="142" alt="Screenshot 2026-06-24 191933" src="https://github.com/user-attachments/assets/574b3d56-4b7d-401c-8dd3-bb0f3aaf2ec5" />
<img width="594" height="128" alt="Screenshot 2026-06-24 191943" src="https://github.com/user-attachments/assets/8d856460-c0b7-42ca-8788-c9a95e6336a8" />

Q 35 :  Sort products by rating in descending order.
select * from sales order by rating DESC;
<img width="594" height="140" alt="Screenshot 2026-06-24 192117" src="https://github.com/user-attachments/assets/2555821b-4a6a-4bde-ac4d-1236fab23224" />
<img width="590" height="130" alt="Screenshot 2026-06-24 192148" src="https://github.com/user-attachments/assets/ba7fccae-4c4b-4ab2-b1f0-087dba2ef572" />

 Q 36 : Display the highest priced product. 
select * from sales order by price DESC limit 1 ;
<img width="584" height="38" alt="image" src="https://github.com/user-attachments/assets/183fa60b-8cfb-4047-9b4b-cbf0af7df895" />

Q 37 : Display the lowest priced product.
select * from sales order by price ASC limit 1 ;
<img width="580" height="33" alt="image" src="https://github.com/user-attachments/assets/63aed5c4-c5e7-48ff-a87f-a9589acfcea7" />

Q 38 : Display the highest rated product. 
select * from sales order by rating DESC limit 1 ;
<img width="588" height="34" alt="image" src="https://github.com/user-attachments/assets/85d3649c-18b6-4f30-befb-712a7837923f" />

Q 39 :  Display the latest order. 
select * from sales order by order_date DESC ; 
<img width="596" height="153" alt="image" src="https://github.com/user-attachments/assets/06156d97-0538-4b79-9962-96b94753bc79" />
<img width="593" height="114" alt="image" src="https://github.com/user-attachments/assets/5e177722-065b-47a2-8a82-99bdd9633f25" />

 Q 40 :  Display the oldest order. 
 select * from sales order by order_date ASC;
 <img width="596" height="143" alt="image" src="https://github.com/user-attachments/assets/1f5f7911-1bb2-4f20-8ef8-789d93a5feb6" />
 <img width="590" height="128" alt="image" src="https://github.com/user-attachments/assets/8a910b87-228a-42f3-a82c-97dddde2dad3" />

Q 41 :  Display the top 5 records. 
 select * from sales limit 5 ;
 <img width="597" height="83" alt="image" src="https://github.com/user-attachments/assets/3e3166f1-f9e8-4d1a-868d-363ad816528e" />

 Q 42 :  Display the top 3 most expensive products.
 select * from sales order by price DESC limit 3;
 <img width="587" height="56" alt="image" src="https://github.com/user-attachments/assets/3815cbc5-ebc5-43ac-92cc-1a5f6ef78940" />

Q 43 : Display the top 5 highest rated products. 
 select * from sales order by rating DESC limit 5 ;
 <img width="592" height="80" alt="image" src="https://github.com/user-attachments/assets/8a010f90-99a1-4e69-8748-bf05c735d899" />

Q 44 :  Display the second highest priced product. 
 select * from sales order by price DESC limit 1 offset 1 ;
 <img width="587" height="28" alt="image" src="https://github.com/user-attachments/assets/e4535a48-4ae1-4102-a0f9-eddcf04231ff" />

 Q 45 : Display the third highest priced product. 
 select * from sales order by price DESC limit 1 offset 2 ;
 <img width="586" height="26" alt="image" src="https://github.com/user-attachments/assets/4eb5790f-f172-4dd9-8444-87f85264f3d0" />

 Q 46 : Skip the first 5 rows and display the next records.
 select * from sales limit 15 offset 5 ;
 <img width="598" height="208" alt="image" src="https://github.com/user-attachments/assets/05a0f3e4-d061-401a-aead-3aa03741c467" />

Q 47: Display rows 6 to 10. 
 select * from sales limit 5 offset 5 ;
 <img width="595" height="81" alt="image" src="https://github.com/user-attachments/assets/0f395781-020a-4ad8-847a-7a8aeffea28f" />

Q 48 :  Display rows 11 to 15. 
 select * from sales limit 5 offset 10 ;
 <img width="596" height="78" alt="image" src="https://github.com/user-attachments/assets/164f2526-70fb-495b-b144-0170fbd2ee72" />

Q 49 :  Display rows 16 to 20.
 select * from sales limit 5 offset 15 ;
 <img width="595" height="86" alt="image" src="https://github.com/user-attachments/assets/d85dec4f-cf1e-4f31-a56f-4eaceef0a29a" />

 Q 50 :  Display the top 3 latest orders.
 select * from sales order by order_date DESC limit 3 ;
 <img width="596" height="54" alt="image" src="https://github.com/user-attachments/assets/e46da493-34c2-47bb-9e67-7b17e7f7b7e1" />

Q 51 : Find the total number of orders.
 select count(*) from sales ;

 <img width="70" height="31" alt="image" src="https://github.com/user-attachments/assets/57b20331-e0b4-4efe-bfca-94964fd387ec" />

Q 52 :  Find the total sales revenue. 
 select sum( price * quantity) as total_revenue from sales ;

 <img width="85" height="29" alt="image" src="https://github.com/user-attachments/assets/42767d20-7631-4341-86b8-785a9d55a4db" />

Q 53 : Find the average sales amount. 
 select avg(price * quantity) as avg_revenue from sales ;

 <img width="85" height="34" alt="image" src="https://github.com/user-attachments/assets/8d03929a-dc80-472d-b221-28a2568c8961" />

 Q 54 :  Find the maximum sales amount.
 select max(price*quantity) as max_sales from sales ;

 <img width="68" height="28" alt="image" src="https://github.com/user-attachments/assets/9f613722-f294-4c89-9860-6f5274343fb9" />

Q 55 :Find the minimum sales amount.
 select min(price*quantity) as min_sales from sales ;

 <img width="68" height="31" alt="image" src="https://github.com/user-attachments/assets/62bc4e0a-69e1-4864-b227-8e7c77973b4e" />

 Q 56 : Find the highest rating. 
 select max(rating) from sales ;

 <img width="83" height="28" alt="image" src="https://github.com/user-attachments/assets/1fa8c12a-bdaa-4f1b-a3a9-004ca2d405f9" />

 Q 57 : Find the lowest rating. 
 select min(rating) from sales ;

 <img width="73" height="29" alt="image" src="https://github.com/user-attachments/assets/e6b98411-d337-48a3-8f9c-730eed20514e" />

Q 58 : Find the average rating.
 select avg(rating) from sales ;

 <img width="74" height="29" alt="image" src="https://github.com/user-attachments/assets/e767d579-0b91-473b-8e55-d9559f577c73" />

Q 59 :  Find the total quantity sold.
 select sum(quantity) as total_quantity from sales;

 <img width="81" height="29" alt="image" src="https://github.com/user-attachments/assets/4e481822-2bb7-46c6-b594-1b94db067076" />

Q 60 :  Find the average quantity sold. 
 select avg(quantity) from sales;

 <img width="82" height="29" alt="image" src="https://github.com/user-attachments/assets/8c7117d7-6265-43aa-a406-5d822db69ff4" />

Q 61 :  Find the maximum quantity sold. 
 select  max(quantity) from sales;

 <img width="87" height="29" alt="image" src="https://github.com/user-attachments/assets/5e0aa96a-0dfb-4bec-9837-3c9ea1c8fcea" />

 Q 62 : Find the minimum quantity sold. 
 select min(quantity) from sales ;

 <img width="80" height="32" alt="image" src="https://github.com/user-attachments/assets/f620d38a-c4e0-4b20-a8ee-a91f03890a7a" />

  Q 63 : Count the number of Electronics products.
 select count(*) from sales where category ="electronics" ;

 <img width="64" height="29" alt="image" src="https://github.com/user-attachments/assets/0a26b6c1-480b-4578-a19c-e38e038773c1" />

Q 64 :  Count the number of Fashion products. 
 select count(*) from sales where category ="fashion";

 <img width="70" height="28" alt="image" src="https://github.com/user-attachments/assets/08c6b267-fb34-440a-b16f-18e32e686fa0" />

Q 65 :  Count the number of Sports products. 
 select count(*) from sales where category = 'sports' ;

 <img width="68" height="31" alt="image" src="https://github.com/user-attachments/assets/82ccf099-d2be-44c6-aaeb-4453360f4a66" />

Q 66 :  Convert all customer names to uppercase. 
 select customer_name, upper(customer_name) from sales ;

 <img width="184" height="154" alt="image" src="https://github.com/user-attachments/assets/878907d7-fc23-4af1-bbb4-1df032164696" />

<img width="185" height="114" alt="image" src="https://github.com/user-attachments/assets/0df5db63-7154-45b4-a560-deb346ca326e" />

Q 67 :  Convert all customer names to lowercase. 
 select customer_name, lower(customer_name) from sales ;

 <img width="184" height="155" alt="image" src="https://github.com/user-attachments/assets/d5c38fc2-621f-4d76-a45d-804a4861b2c0" />

 <img width="186" height="114" alt="image" src="https://github.com/user-attachments/assets/ed2a7c11-3573-4e67-a1dd-a85cb395f800" />

Q 68 :  Find the length of each customer name = 
 select customer_name, length(customer_name) from sales ;

 <img width="191" height="153" alt="image" src="https://github.com/user-attachments/assets/a264ab78-75b2-461b-b38b-6b30c68a1725" />

<img width="183" height="117" alt="image" src="https://github.com/user-attachments/assets/a6d1809d-c33a-437b-9d10-317eb37e0afe" />

Q 69 : Find the length of each city name = 
 select city, length(city) from sales ;

 <img width="111" height="142" alt="image" src="https://github.com/user-attachments/assets/16192599-fe1b-400e-ab12-34fb9a26d046" />

<img width="104" height="126" alt="image" src="https://github.com/user-attachments/assets/895be504-7680-4805-be05-f151824e1638" />

 Q 70 : Combine customer name and city in one column = 
 select concat(customer_name, '_', city) from sales ;

 <img width="146" height="161" alt="image" src="https://github.com/user-attachments/assets/8a05478c-4fea-4462-ac1e-7b06641d5b80" />

 <img width="135" height="115" alt="image" src="https://github.com/user-attachments/assets/8f399d28-be03-4745-abbd-376919198a40" />

Q 71 : Replace the letter 'a' with '@' in customer names.
 select replace(customer_name,'a','@') from sales ;

 <img width="146" height="152" alt="image" src="https://github.com/user-attachments/assets/5fb4c351-7a0c-40dc-8893-b2c10c23cfa1" />

 <img width="112" height="114" alt="image" src="https://github.com/user-attachments/assets/fe423768-5c37-424e-af83-4d0f69d1df16" />

 Q 72 : Replace the letter 'e' with '*' in customer names. 
 select replace(customer_name,'e','*') from sales ;

 <img width="136" height="155" alt="image" src="https://github.com/user-attachments/assets/b30427e3-5d2a-49f0-b9ec-08f59e76666a" />

 <img width="139" height="113" alt="image" src="https://github.com/user-attachments/assets/5a5285de-9e10-46de-b0ff-2d3b131e8013" />

Q 73 : Remove extra spaces using TRIM(). 
 select trim(sale_id), trim(customer_name), trim(gender) ,trim(age), trim(city) , trim(category), trim(product_name), trim(payment_mode), trim(quantity), trim(price), trim(rating),trim(order_date) from sales ;

 <img width="458" height="140" alt="image" src="https://github.com/user-attachments/assets/d483e3d3-e051-46dc-b5ac-20a5ebe48295" />

<img width="316" height="152" alt="image" src="https://github.com/user-attachments/assets/55786ae0-3c65-4f80-81c3-0744fdee84a8" />

<img width="460" height="130" alt="image" src="https://github.com/user-attachments/assets/932b14e5-3238-4217-a0bd-4c4e0ab23403" />

<img width="310" height="130" alt="image" src="https://github.com/user-attachments/assets/614e1a5f-1e28-44c9-b608-bb188ae99d88" />

Q 74 : Display the first 3 letters of each customer name. 
 select substring(customer_name,1,3) from sales ;

 <img width="143" height="152" alt="image" src="https://github.com/user-attachments/assets/0ef7628a-2062-4711-9d72-fcdd3569d196" />

<img width="140" height="115" alt="image" src="https://github.com/user-attachments/assets/236e3a51-19bf-4e4a-b182-04968aee42ac" />

Q 75 :  Display the last 2 letters of each city name. 
 select city ,substring( city, length(city)-1,3) from sales ;

 <img width="185" height="194" alt="image" src="https://github.com/user-attachments/assets/572d0198-1db7-4dc8-a565-1f0d3820df6c" />

<img width="179" height="86" alt="image" src="https://github.com/user-attachments/assets/9384b65a-8ed7-497d-ab24-248c0645c66d" />

Q 76 : Round all prices.
 select round(price) from sales ;

 <img width="76" height="142" alt="image" src="https://github.com/user-attachments/assets/7cc737a3-4bb1-415f-9b86-7df46638a307" />

<img width="74" height="124" alt="image" src="https://github.com/user-attachments/assets/1563ce3a-b031-4789-8db3-d7f1c35e0dbe" />

Q 77 :  Apply CEIL() on prices. 
 select ceil(price) from sales ;

 <img width="66" height="140" alt="image" src="https://github.com/user-attachments/assets/c44a17ed-12c9-433b-8191-570ba6b28fd0" />

<img width="64" height="130" alt="image" src="https://github.com/user-attachments/assets/a8ee7604-370b-47f8-aeab-2c2a11a4283c" />

 Q 78 :  Apply FLOOR() on prices. 
 select floor(price) from sales ;

 <img width="68" height="143" alt="image" src="https://github.com/user-attachments/assets/7a52e621-c30a-4600-9c6c-c1f007388e49" />

<img width="68" height="127" alt="image" src="https://github.com/user-attachments/assets/06d7a115-caa3-4fdb-a623-f0a2f1704c6a" />

 Q 79 :  Find MOD(quantity,2).
 select mod(quantity,2) from sales ;

 <img width="86" height="218" alt="image" src="https://github.com/user-attachments/assets/1378e0ea-de86-4d3f-b928-ef50bacfdab9" />

<img width="85" height="62" alt="image" src="https://github.com/user-attachments/assets/154fd0c8-0888-425a-92a4-1acc47fd8f96" />

Q 80 :  Find MOD(quantity,3). 
select mod(quantity,3) from sales ;

<img width="85" height="158" alt="image" src="https://github.com/user-attachments/assets/9d911438-d910-42ed-ac33-125672482c81" />

<img width="77" height="115" alt="image" src="https://github.com/user-attachments/assets/7f9b4b39-a638-47cf-b577-588e663034cb" />

 Q 81 :  Display the current time. 
select curtime() ;

<img width="65" height="31" alt="image" src="https://github.com/user-attachments/assets/21b94930-acfa-4cb8-8643-683e5f483f2c" />

Q 82 :  Display the current date.
select curdate() ;

<img width="74" height="32" alt="image" src="https://github.com/user-attachments/assets/6b2298b0-5a50-4a54-88ed-a9cb632f53d1" />

 Q 83 :  Display the current timestamp. 
select now() ;

<img width="113" height="34" alt="image" src="https://github.com/user-attachments/assets/80cd16b6-6bb9-4cb6-92cd-90a90f85a21b" />

Q 84 : Extract the year from order_date.
select year(order_date) from sales ;

<img width="95" height="230" alt="image" src="https://github.com/user-attachments/assets/ca2a7d57-fdcc-4021-9327-b324657c64f9" />

<img width="96" height="50" alt="image" src="https://github.com/user-attachments/assets/35b0d027-27a7-4935-a7d1-6b746bff1191" />

Q 85 : Extract the month from order_date. 
select month(order_date) from sales ;

<img width="100" height="230" alt="image" src="https://github.com/user-attachments/assets/db1ae691-fd83-4ab4-9ed0-2e329f6ed64a" />

<img width="99" height="50" alt="image" src="https://github.com/user-attachments/assets/155caaad-26dc-4d3b-a578-4d264d93ad31" />

Q 86 : Extract the day from order_date = 
select day (order_date) from sales ;

<img width="96" height="164" alt="image" src="https://github.com/user-attachments/assets/b7453733-0a83-4c73-ad5f-338f1617c594" />

<img width="101" height="113" alt="image" src="https://github.com/user-attachments/assets/f9f6d6ce-4623-42d5-a20c-bd650cc45f9b" />

Q 87 :  Display orders placed in January.
select * from sales where month(order_date) =1;

<img width="592" height="145" alt="image" src="https://github.com/user-attachments/assets/1d7b6643-bde8-4bed-941e-9f92a99b3d84" />

<img width="594" height="127" alt="image" src="https://github.com/user-attachments/assets/67273654-5858-4e3b-a26f-fbcb3bff7c9f" />

 Q 88 :  Display orders placed before 20 January 2026.
select * from sales where order_date <'2026-01-20' ;

<img width="593" height="146" alt="image" src="https://github.com/user-attachments/assets/9c74b7ca-7216-4eb6-a7bb-2ad98ae3d95a" />

Q 89 : Display orders placed after 20 January 2026. 
select * from sales where order_date >'2026-01-20' ;

<img width="591" height="129" alt="image" src="https://github.com/user-attachments/assets/44ee082a-5fac-4d2d-a99f-cdae071b4244" />

Q 90 :  Display the latest order date.
select * from sales order by order_date DESC limit 1 ;

<img width="577" height="31" alt="image" src="https://github.com/user-attachments/assets/db35414e-b191-418e-916f-53ea7bb3e602" />

Q 91 : Update the city of Akash. 
update sales set city ='mumbai' where sale_id= 1 ;
Query OK, 0 rows affected (0.00 sec)
Rows matched: 1  Changed: 0  Warnings: 0

Q 92 :  Update the rating of Rahul. 
update sales set rating =4.9 where customer_name ='rahul' ;
Query OK, 0 rows affected (0.00 sec)
Rows matched: 1  Changed: 0  Warnings: 0

Q 93 :  Change all Card payments to UPI. 
update sales set payment_mode ='UPI' where payment_mode ='card';
Query OK, 8 rows affected (0.00 sec)
Rows matched: 8  Changed: 8  Warnings: 0

Q 94 :  Increase all product prices by 500. 
update sales set price =price+ 500 ;
Query OK, 20 rows affected (0.01 sec)
Rows matched: 20  Changed: 20  Warnings: 0

Q 95 : Decrease all product prices by 100. 
update sales set price =price-100 ;
Query OK, 20 rows affected (0.01 sec)
Rows matched: 20  Changed: 20  Warnings: 0

Q 96 : Change category Electronics to Gadgets.
update sales set category = 'gadgets' where category ='electronics' ;
Query OK, 7 rows affected (0.01 sec)
Rows matched: 7  Changed: 7  Warnings: 0

Q 97 : Change city Pune to Nagpur. 
update sales set city='Nagpur' where city ='pune' ;
Query OK, 5 rows affected (0.00 sec)
Rows matched: 5  Changed: 5  Warnings: 0

Q 98 :  Update the quantity of a selected product. 
update sales set quantity =5 where product_name ='laptop' ;
Query OK, 1 row affected (0.00 sec)
Rows matched: 1  Changed: 1  Warnings: 0

Q 99 :  Update a product name. 
update sales set product_name ='Hand bag' where product_name ='football' ;
Query OK, 1 row affected (0.01 sec)
Rows matched: 1  Changed: 1  Warnings: 0

Q 100 : Update a customer name.
update sales set customer_name ='pranita' where customer_name ='karan' ;
Query OK, 1 row affected (0.01 sec)
Rows matched: 1  Changed: 1  Warnings: 0

Q 101 :  Delete a specific customer record.
delete from sales where customer_name ='harsh' ;
Query OK, 1 row affected (0.01 sec)

Q 102 :  Delete all Sports category records. 
delete from sales where category = 'sports' ;
Query OK, 3 rows affected (0.01 sec)

Q 103 :  Delete records with rating below 4.0. 
delete from sales where rating <4.0 ;
Query OK, 0 rows affected (0.00 sec)

Q 104 : Delete all Cash payment records. 
delete from sales where payment_mode ='cash';
Query OK, 1 row affected (0.00 sec)

 Q 105 : Delete records from Jaipur.
delete from sales where city ='jaipur';
Query OK, 2 rows affected (0.00 sec)

Q 106 : Display city-wise order count. 
select city,count(*) from sales group by city;
<img width="98" height="68" alt="image" src="https://github.com/user-attachments/assets/cf94542e-b582-40f5-832f-8b6b28bc3ee9" />

Q 107 :Display category-wise order count.
select category, count(*) from sales group by category ;
<img width="104" height="55" alt="image" src="https://github.com/user-attachments/assets/97ae9d8a-68cd-44b4-97b4-2728b75ef92e" />

Q 108 :  Display payment mode-wise order count.
select payment_mode ,count(*) from sales group by payment_mode ;
<img width="130" height="29" alt="image" src="https://github.com/user-attachments/assets/6916c472-d418-47a4-ac26-9af40afd211f" />

Q 109 : Display gender-wise order count. 
select gender ,count(*) from sales group by gender ;
<img width="98" height="41" alt="image" src="https://github.com/user-attachments/assets/b5e75a8d-9838-4bd9-8fd0-d8340bb66e09" />

Q 110 :  Display city-wise total revenue.
select city,sum(price * quantity) as total_revenue from sales group by city ;
<img width="124" height="68" alt="image" src="https://github.com/user-attachments/assets/b7040d34-f1ff-4964-b28a-0fa8cb76b9f8" />

 Q 111 :  Display category-wise total revenue. 
select category, sum(price * quantity) as total_revenue from sales group by category ;
<img width="126" height="54" alt="image" src="https://github.com/user-attachments/assets/9308c1c7-dd41-4d2f-a75f-0004b20716d7" />

Q 112 :  Display payment mode-wise total revenue.
select payment_mode, sum(price*quantity) as total_revenue from sales group by payment_mode;
<img width="153" height="29" alt="image" src="https://github.com/user-attachments/assets/ef65da3f-e5c5-40ed-a4c0-78c26fa78b0a" />

Q 113 :  Display city-wise average revenue.
select city, avg(price*quantity) as avg_revenue from sales group by city;
<img width="122" height="65" alt="image" src="https://github.com/user-attachments/assets/1131ebe0-5fc2-46dd-88de-24f5378b782c" />

Q 114 : Display category-wise average revenue. 
select category, avg(price * quantity) as avg_revenue from sales group by category;
<img width="126" height="50" alt="image" src="https://github.com/user-attachments/assets/38e1c602-abda-4a62-ae14-6e18fef304ef" />

 Q 115 :  Display city-wise maximum sale. 
select city , max(price*quantity) as max_revenue from sales group by city;
<img width="116" height="68" alt="image" src="https://github.com/user-attachments/assets/23e7f75b-1868-4cb4-bf02-328108b1817f" />

 Q 116 :  Display city-wise minimum sale. 
select city , min(price * quantity) as min_revenue from sales group by city ;
<img width="115" height="67" alt="image" src="https://github.com/user-attachments/assets/7539a488-e9e9-4414-beda-ddbd72e15fe1" />

Q 117 :  Display category-wise maximum sale. 
select category , max(price * quantity)as max_revenue from sales group by category ;
<img width="128" height="53" alt="image" src="https://github.com/user-attachments/assets/80f02eb7-f73e-4127-a205-6c27ac914bf9" />

Q 118 :  Display category-wise minimum sale.
select category , min(price * quantity) as min_revenue from sales group by category ;
<img width="128" height="53" alt="image" src="https://github.com/user-attachments/assets/5617cdc2-0a74-46ff-8000-4122b4380908" />

 Q 119 : Display city and category-wise revenue.
select city,category , sum(price*quantity) as total_revenue from sales group by city,category ;
<img width="163" height="130" alt="image" src="https://github.com/user-attachments/assets/a7babb7b-9e48-47ff-a2e5-fb68c8ca8445" />

Q 120 : Display city and payment mode-wise revenue.
select city,payment_mode ,sum(price*quantity) as total_revenue from sales group by city,payment_mode ;
<img width="191" height="65" alt="image" src="https://github.com/user-attachments/assets/75339692-455b-414e-af29-d83653590ee4" />

Q 121 : Display cities having total revenue greater than 50,000.
select city, sum(price *quantity)as total_revenue from sales group by city having sum(price * quantity) > 50000;
<img width="119" height="41" alt="image" src="https://github.com/user-attachments/assets/e4ba41ab-6785-4adf-97fe-d8c4bd7b34e9" />

Q 122 : Display categories having total revenue greater than 60,000.
select category , sum(price *quantity) as total_revenue from sales group by category having sum(price*quantity) >60000;
<img width="127" height="26" alt="image" src="https://github.com/user-attachments/assets/7d5517de-3308-4268-a603-b6f7ce48f600" />

Q 123 : Display cities having average sale greater than 10,000. 
select city, avg(price * quantity) as avg_sales from sales group by city having sum(price * quantity) >10000;
<img width="121" height="68" alt="image" src="https://github.com/user-attachments/assets/9bcdac7f-6d21-4e65-bda8-a9f40a7557de" />

Q 124 :  Display categories having average rating greater than 4.5.
select category ,avg(rating) from sales group by category having avg(rating) >4.5;
<img width="116" height="40" alt="image" src="https://github.com/user-attachments/assets/d841fa62-ead7-49f2-a5d0-cc2fb6526251" />

Q 125 : Display cities having more than 3 orders. 
Select city ,count(*) from sales group by city having count(*) >3 ;
<img width="103" height="38" alt="image" src="https://github.com/user-attachments/assets/be16c761-db1f-4549-ba61-83f16e744b53" />

Q 126 :  Display categories having more than 2 orders.
select category , count(*) from sales group by category having count(*)>2 ;
<img width="108" height="40" alt="image" src="https://github.com/user-attachments/assets/cf0124fd-1465-4a3e-bc6a-aa40271e47f6" />

Q 127 :  Display payment modes having more than 5 orders.
select payment_mode , count(*) from sales group by payment_mode having count(*) >5 ;
<img width="133" height="26" alt="image" src="https://github.com/user-attachments/assets/07d5d218-984d-4e16-919c-9a14f4c870e1" />

Q 128 :  Display cities having maximum sale greater than 40,000.
select city , max( price * quantity) as max_revenue from sales group by city having max(price*quantity) >40000;
<img width="125" height="44" alt="image" src="https://github.com/user-attachments/assets/c6a58441-a87a-4cec-aaa0-4531a1cd44c1" />

 Q 129 :  Display categories having minimum sale greater than 1,500.
select category ,min(price *quantity) as min_revenue from sales group by category having min(price *quantity)>1500;
<img width="123" height="55" alt="image" src="https://github.com/user-attachments/assets/4c7d3a70-21c3-47d0-9894-05f7e7a46275" />

Q 130 : Display cities having average age greater than 25. 
select city , avg(age) from sales group by city having avg(age) > 25;
<img width="102" height="41" alt="image" src="https://github.com/user-attachments/assets/64ec5831-cafa-4728-af8f-353f8ca3ec18" />
