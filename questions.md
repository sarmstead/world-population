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