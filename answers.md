## Example:
1.
 - `SQL:`
    SELECT count(\*) from items

 - `ANSWER:`
   100

---

1.
 - `SQL:`
    select * from users;

 - `ANSWER:`
   50



2.
 - `SQL:`
  select title from items order by price DESC limit 5

 - `ANSWER:`
 Small Cotton Gloves   |
| Small Wooden Computer |
| Awesome Granite Pants |
| Sleek Wooden Hat      |
| Ergonomic Steel Car

3.
 - `SQL:`
 select category, description from items where category = 'Books' order by price


 - `ANSWER:`
 +------------+---------------------------------------+
| category   | description                           |
|------------+---------------------------------------|
| Books      | De-engineered bi-directional portal   |
| Books      | Implemented non-volatile model        |
| Books      | Reverse-engineered modular hierarchy  |
| Books      | Advanced attitude-oriented encryption |
+------------+---------------------------------------+

 4.
  - `SQL:`
select first_name, last_name from users, addresses where users.id = addresses.user_id and street = '6439 Zetta Hills'

  - `ANSWER:`
  +--------------+-------------+
| first_name   | last_name   |
|--------------+-------------|
| Corrine      | Little      |
+--------------+-------------+

 5.
   - `SQL:`
   update addresses set city = 'New York', state = 'NY', zip = '10108'  where id=41


   - `ANSWER:`
   +------+----------+---------+-------+
   |   id | city     | state   |   zip |
   |------+----------+---------+-------|
   |   41 | New York | NY      | 10108 |
   +------+----------+---------+-------+
  6.
    - `SQL:`
    select sum(price) from items where category = 'Tools'


    - `ANSWER:`
    +-------+
    |   sum |
    |-------|
    |  7383 |
    +-------+
  7.
   - `SQL:`
select sum(quantity) from orders

   - `ANSWER:`
   +-------+
   |   sum |
   |-------|
   |  2125 |
   +-------+
  8.
    - `SQL:`
select sum(price * quantity) from orders, items where  orders.item_id = items.id  and category = 'Books'

    - `ANSWER:`
    +--------+
    |    sum |
    |--------|
    | 420566 |
    +--------+

    9.
      - `SQL:`
      insert into users(id, first_name, last_name, email) values(123, 'Jasmine', 'Frantz', 'jasminefrantz@gmail.com')
      insert into orders(user_id, item_id, quantity) values(123, 100, 12)

      - `ANSWER:`

      |   45 | Kayden       | DuBuque     | gage.langworth@millsturcotte.net  |
|   46 | Derrick      | Cummerata   | libby.langosh@hodkiewicz.com      |
|   47 | Colton       | Crooks      | declan_mclaughlin@carroll.biz     |
|   48 | Roselyn      | Zboncak     | jeyca@pfannerstill.com            |
|   49 | Ignacio      | Buckridge   | chance@wiegand.name               |
|   50 | Norene       | Bartell     | natalie@cainkeeling.biz           |
|  123 | Jasmine      | Frantz      | hyunfrantz@gmail.com              |
+------+--------------+-------------+-----------------------------------+

|  372 |        49 |         6 |          6 | 2015-02-09 00:40:31.294004 |
|  373 |        49 |        87 |          7 | 2015-02-09 00:40:31.299549 |
|  374 |        50 |        49 |          7 | 2015-02-09 00:40:31.30199  |
|  375 |        50 |         2 |          6 | 2015-02-09 00:40:31.303884 |
|  376 |        50 |        56 |          9 | 2015-02-09 00:40:31.305783 |
|  377 |        50 |        91 |          2 | 2015-02-09 00:40:31.307668 |
|    1 |       123 |       100 |         12 | <null>                     |
+------+-----------+-----------+------------+----------------------------+


++++ Adventure Mode +++++

1.  - `SQL:`
select title from items, orders where items.id = orders.item_id order by quantity DESC limit 1
  - `ANSWER:`
  +-----------------------+
| title                 |
|-----------------------|
| Awesome Granite Pants |
+-----------------------+

2.  - `SQL:`
select first_name, last_name from users, orders, items  where users.id = orders.user_id and items.id = orders.item_id order by (price*quantity) DESC limit 2

  - `ANSWER:`

  +--------------+-------------+
  | first_name   | last_name   |
  |--------------+-------------|
  | Jasmine      | Frantz      |
  | Missouri     | Carroll     |
  +--------------+-------------+

## ooops if the answer is correct, it happens to be me! create.sql doesn't seem like it's updated on github. With older list, the answer would be 'Missouri Carroll'

3. - `SQL:`
 select sum(price*quantity) as automotive from items, orders where items.id = orders.item_id and category like 'Automotive%'

 +--------------+
|   automotive |
|--------------|
|       170684 |
+--------------+

select sum(price*quantity) as baby from items, orders where items.id = orders.item_id and category like 'baby%'

select sum(price*quantity) as books from items, orders where items.id = orders.item_id and category like 'Books%'


select sum(price*quantity) as beauty from items, orders where items.id = orders.item_id and category like 'Beauty%'

select sum(price*quantity) as beauty from items, orders where items.id = orders.item_id and category like 'Clothing%'

select sum(price*quantity) as beauty from items, orders where items.id = orders.item_id and category like 'Computers%'

select sum(price*quantity) as beauty from items, orders where items.id = orders.item_id and category like 'Electronics%'

select sum(price*quantity) as beauty from items, orders where items.id = orders.item_id and category like 'Games%'

select sum(price*quantity) as beauty from items, orders where items.id = orders.item_id and category like 'Garden%'

select sum(price*quantity) as beauty from items, orders where items.id = orders.item_id and category like 'Grocery%'

select sum(price*quantity) as beauty from items, orders where items.id = orders.item_id and category like 'Health%'

select sum(price*quantity) as beauty from items, orders where items.id = orders.item_id and category like 'Home%'

select sum(price*quantity) as beauty from items, orders where items.id = orders.item_id and category like 'Industrial%'
select sum(price*quantity) as beauty from items, orders where items.id = orders.item_id and category like 'Jewelery%'
select sum(price*quantity) as beauty from items, orders where items.id = orders.item_id and category like 'Kids%'
select sum(price*quantity) as beauty from items, orders where items.id = orders.item_id and category like 'Movie%'
select sum(price*quantity) as beauty from items, orders where items.id = orders.item_id and category like 'Music%'
select sum(price*quantity) as beauty from items, orders where items.id = orders.item_id and category like 'Outdoors%'
select sum(price*quantity) as beauty from items, orders where items.id = orders.item_id and category like 'Kids%'
select sum(price*quantity) as beauty from items, orders where items.id = orders.item_id and category like 'Kids%'
select sum(price*quantity) as beauty from items, orders where items.id = orders.item_id and category like 'Kids%'



- `ANSWER:`

# in a relation to 5...
select addresses.id, city, state, zip from users, addresses where users.id = addresses.user_id and first_name ='Virginie' and last_name = 'Mitchell'

select.. these...
from database
these items...

#9

you have to specify the columns
insert into orders(user_id,item_id,quantity) values(123, 100, 12)

In that case you don’t have to list out all the columns after `INSERT INTO users`
If you are specifying every value (in column order) then you can leave off that part
