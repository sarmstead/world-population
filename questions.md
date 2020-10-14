# Database Questions
## 1. What years are covered by the dataset?
The years 2000-2010.

Code used: 
> `SELECT DISTINCT year from population_years;`

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