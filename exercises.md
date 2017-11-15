1. SELECT id FROM authors WHERE name = 'Kara Melton’;

 id
----
  8
(1 row)

SELECT title FROM articles WHERE author_id = 8

 How Tech Business Models Come From Marginalized Communities, But Startups Are Still Mostly White
 Confronting the Assumption of Whiteness in Virtual Spaces

2. SELECT id FROM provinces WHERE name = 'Ontario’;

 id
----
 14
(1 row)

 SELECT name FROM cities WHERE province_id = 14;

  name   
---------
 Toronto
 Ottawa
(2 rows)

3. SELECT author_id FROM articles WHERE title = 'Coding Bootcamps and Emotional Labor';

 author_id
-----------
         4
(1 row)

one_to_many_assignment=# SELECT name FROM authors WHERE id = 4;

       name        
-------------------
 Tilde Ann Thurium
(1 row)

4. SELECT id FROM countries WHERE name = 'Canada';

 id
----
  1
(1 row)

SELECT COUNT(*) FROM provinces WHERE country_id = 1;

 count
-------
    14
(1 row)

5. SELECT id FROM residences WHERE address = '4740 McDermott Street';

 id
----
  9
(1 row)

one_to_many_assignment=# SELECT COUNT(name) FROM persons WHERE residence_id = 9;       

 count
-------
     2
(1 row)

6. SELECT city_id FROM residences WHERE address = '4740 McDermott Street';

 city_id
---------
      11
(1 row)

SELECT name FROM cities WHERE id = 11;

  name  
--------
 Ottawa
(1 row)

7. SELECT city_id FROM residences WHERE address = '4740 McDermott Street';

SELECT province_id FROM cities WHERE id = 11;
 province_id
-------------
          14
(1 row)

SELECT name FROM provinces WHERE id = 14;

  name   
---------
 Ontario
(1 row)

8. SELECT city_id FROM residences WHERE address = '4740 McDermott Street';

SELECT province_id FROM cities WHERE id = 11;

SELECT country_id FROM provinces WHERE id = 14;

 country_id
------------
          1
(1 row)

one_to_many_assignment=# SELECT name FROM countries WHERE id = 1;

  name  
--------
 Canada
(1 row)

9. SELECT residence_id FROM persons WHERE name = 'Destini Davis';

 residence_id
--------------
            2
(1 row)

SELECT city_id FROM residences WHERE id = 2;

 city_id
---------
       8
(1 row)

SELECT province_id FROM cities WHERE id = 8;

 province_id
-------------
          14
(1 row)

SELECT country_id FROM provinces WHERE id = 14;

 country_id
------------
          1
(1 row)

SELECT name FROM countries WHERE id = 1;

  name  
--------
 Canada
(1 row)

10. SELECT id FROM authors WHERE name = 'Aditya Mukerjee';

 id
----
  2
(1 row)

SELECT COUNT(*) FROM articles WHERE author_id = 2;
open
 count
-------
     1
(1 row)
