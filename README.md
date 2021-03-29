# 03----Manipulation-des-donn-es-PHP-

mysql> UPDATE school
    -> SET country = Sweden
    -> WHERE id = 3;
ERROR 1054 (42S22): Unknown column 'Sweden' in 'field list'
mysql> UPDATE school
    -> SET country = 'Sweden'
    -> WHERE name = 'Durmstrang Institute';
Query OK, 1 row affected (0.01 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql> SELECT * FROM school;
+----+---------------------------------------------+----------+----------------+
| id | name                                        | capacity | country        |
+----+---------------------------------------------+----------+----------------+
|  1 | Beauxbatons Academy of Magic                |      550 | France         |
|  2 | Castelobruxo                                |      380 | Brazil         |
|  3 | Durmstrang Institute                        |      570 | Sweden         |
|  4 | Hogwarts School of Withcraft and Wizardy    |      450 | United Kingdom |
|  5 | Ilvermorny School of Witchcraft and Wizardy |      300 | USA            |
|  6 | Koldovstoretz                               |      125 | Russia         |
|  7 | Mahoutokoro School of Magic                 |      800 | Japan          |
|  8 | Uagadou School of Magic                     |      350 | Uganda         |
+----+---------------------------------------------+----------+----------------+
8 rows in set (0.00 sec)

mysql> UPDATE school
    -> SET capacity = 700
    -> WHERE name = 'Mahoutokoro School of Magic';
Query OK, 1 row affected (0.01 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql> SELECT * FROM school;
+----+---------------------------------------------+----------+----------------+
| id | name                                        | capacity | country        |
+----+---------------------------------------------+----------+----------------+
|  1 | Beauxbatons Academy of Magic                |      550 | France         |
|  2 | Castelobruxo                                |      380 | Brazil         |
|  3 | Durmstrang Institute                        |      570 | Sweden         |
|  4 | Hogwarts School of Withcraft and Wizardy    |      450 | United Kingdom |
|  5 | Ilvermorny School of Witchcraft and Wizardy |      300 | USA            |
|  6 | Koldovstoretz                               |      125 | Russia         |
|  7 | Mahoutokoro School of Magic                 |      700 | Japan          |
|  8 | Uagadou School of Magic                     |      350 | Uganda         |
+----+---------------------------------------------+----------+----------------+
8 rows in set (0.00 sec)

mysql> DELETE from school
    -> WHERE name LIKE '%Magic%';
Query OK, 3 rows affected (0.01 sec)

mysql> SELECT * FROM school;
+----+---------------------------------------------+----------+----------------+
| id | name                                        | capacity | country        |
+----+---------------------------------------------+----------+----------------+
|  2 | Castelobruxo                                |      380 | Brazil         |
|  3 | Durmstrang Institute                        |      570 | Sweden         |
|  4 | Hogwarts School of Withcraft and Wizardy    |      450 | United Kingdom |
|  5 | Ilvermorny School of Witchcraft and Wizardy |      300 | USA            |
|  6 | Koldovstoretz                               |      125 | Russia         |
+----+---------------------------------------------+----------+----------------+
5 rows in set (0.00 sec)

mysql> SELECT * FROM school;
+----+---------------------------------------------+----------+----------------+
| id | name                                        | capacity | country        |
+----+---------------------------------------------+----------+----------------+
|  2 | Castelobruxo                                |      380 | Brazil         |
|  3 | Durmstrang Institute                        |      570 | Sweden         |
|  4 | Hogwarts School of Withcraft and Wizardy    |      450 | United Kingdom |
|  5 | Ilvermorny School of Witchcraft and Wizardy |      300 | USA            |
|  6 | Koldovstoretz                               |      125 | Russia         |
+----+---------------------------------------------+----------+----------------+
5 rows in set (0.00 sec)

mysql> 
