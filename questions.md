# Database Questions
## 1. What years are covered by the dataset?
The dataset covers the years 2000-2010.

Code used: 
> `SELECT DISTINCT year` 

>  `FROM population_years;`

## 2. What is the largest population size for Gabon in this dataset?
The largest population size for Gabon in this dataset is 1.54526 million.

Code used: 
> `SELECT population`

> `FROM population_years`

> `WHERE country = 'Gabon'`

> `ORDER BY year DESC;`

## 3. What were the 10 lowest population countries in 2005?
In 2005, the 10 lowest population countries were:
Country | Population (millions)
--- | --- 
Niue | 0.00216
Falkland Islands (Islas Malvinas) | 0.00297
Montserrat | 0.00453
Saint Pierre and Miquelon | 0.0062
Saint Helena | 0.00748
Nauru | 0.01001
Cook Islands | 0.0136
Turks and Caicos Island | 0.02057
Virgin Islands, British | 0.02268
Gibraltar | 0.02846

Code used:
> `SELECT country, population`

> `FROM population_years`

> `WHERE year = '2005'`

> `ORDER BY population ASC`

> `LIMIT 10;`

## 4. What are all the distinct countries with a population of over 100 million in the year 2010?
In 2010, the countries with a population of over 100 million were:
Country | Population (millions)
--- | ---
China | 1330.14129
India | 1173.10802
United States | 310.23286
Indonesia | 242.96834
Brazil | 201.10333
Pakistan | 184.40479
Bangladesh | 156.11846
Nigeria | 152.21734
Russia | 139.39021
Japan | 126.80443
Mexico | 112.46886

Code used:
> `SELECT DISTINCT country, population`

> `FROM population_years`

> `WHERE population > 100`

> `AND year = 2010`

> `ORDER BY population DESC;`

## 5. How many countries in this dataset have the word “Islands” in their name?
There are 9 countries in this dataset that have the word "Islands" in their name:

1. Cayman Islands
2. Cook Islands
3. Falkland Islands (Islas Malvinas)
4. Faroe Islands
5. Solomon Islands
6. Turks and Caicos Islands
7. U.S. Pacific Islands
8. Virgin Islands,  U.S.
9. Virgin Islands, British

Code used:
>`SELECT DISTINCT country`

>`FROM population_years`

>`WHERE country LIKE '%Islands%'`

>`ORDER BY country ASC;`

## 6. What is the difference in population between 2000 and 2010 in Indonesia?
The difference in population between 2000 and 2010 is 28.29173 million. Below is the dataset returned from this query:
Year | Country | Population (millions)
--- | --- | ---
2000 | Indonesia | 214.67661
2001 | Indonesia | 217.83628
2002 | Indonesia | 220.97191
2003 | Indonesia | 223.06967
2004 | Indonesia | 226.00413
2005 | Indonesia | 228.89575
2006 | Indonesia | 231.82024
2007 | Indonesia | 234.694
2008 | Indonesia | 237.51236
2009 | Indonesia | 240.27152
2010 | Indonesia | 242.96834

Code used:
> `SELECT year, country, population`

> `FROM population_years`

> `WHERE country = 'Indonesia'`

> `AND year BETWEEN 2000 AND 2010`

> `ORDER BY year ASC;`