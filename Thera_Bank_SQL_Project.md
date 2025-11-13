**List of Queries operated on SQLite Online:**

* Query 1

SELECT \* FROM Bank\_Personal\_Loan\_Modelling LIMIT 5;



* Query 2

PRAGMA table\_info(Bank\_Personal\_Loan\_Modelling)



* Query 3

SELECT 

&nbsp;   ROUND(AVG(Income),2) AS AvgIncome, Education 

FROM 

&nbsp;   Bank\_Personal\_Loan\_Modelling 

GROUP BY 

&nbsp;   Education;



* Query 4

SELECT 

&nbsp;   Family, 

&nbsp;   SUM(Personal\_Loan) AS Loan\_Takers, 

&nbsp;   ROUND(SUM(Personal\_Loan)\*100.0/COUNT(\*), 2) AS Loan\_Acceptance\_Rate\_Percent 

FROM 

&nbsp;   Bank\_Personal\_Loan\_Modelling 

GROUP BY 

&nbsp;   Family 

ORDER BY 

&nbsp;   Family;



* Query 5

SELECT

&nbsp;   CASE

&nbsp;       WHEN Income < 40 THEN 'Below 40k'

&nbsp;       WHEN Income BETWEEN 40 AND 60 THEN '40k - 60k'

&nbsp;       WHEN Income BETWEEN 61 AND 80 THEN '61k - 80k'

&nbsp;       WHEN Income BETWEEN 81 AND 100 THEN '81k - 100k'

&nbsp;       ELSE 'Above 100k'

&nbsp;   END AS Income\_Range,

&nbsp;   COUNT(\*) AS Total\_Customers,

&nbsp;   SUM(Personal\_Loan) AS Loan\_Takers,

&nbsp;   ROUND(SUM(Personal\_Loan) \* 100.0 / COUNT(\*), 2) AS Loan\_Acceptance\_Rate\_Percent

FROM 

&nbsp;   Bank\_Personal\_Loan\_Modelling

GROUP BY 

&nbsp;   Income\_Range

ORDER BY 

&nbsp;   Income\_Range;



* Query 6

SELECT 

&nbsp;   Education, 

&nbsp;   SUM(Personal\_Loan) AS Loan\_Takers, 

&nbsp;   ROUND(SUM(Personal\_Loan)\*100.0/COUNT(\*), 2) AS Loan\_Acceptance\_Rate\_Percent 

FROM 

&nbsp;   Bank\_Personal\_Loan\_Modelling 

GROUP BY 

&nbsp;   Education 

ORDER BY 

&nbsp;   Education;

* Query 7

SELECT 

&nbsp;   CASE 

&nbsp;      WHEN CreditCard=1 THEN 'Credit Card User'

&nbsp;   ELSE 'Non Credit Card User'

&nbsp;   END AS Credit\_Card\_Usage,

&nbsp;   SUM(Personal\_Loan) AS Loan\_Takers, 

&nbsp;   ROUND(SUM(Personal\_Loan)\*100.0/COUNT(\*), 2) as Loan\_Acceptance\_Rate\_Percent 

FROM 

&nbsp;   Bank\_Personal\_Loan\_Modelling

GROUP BY 

&nbsp;   Credit\_Card\_Usage 

ORDER BY 

&nbsp;   Credit\_Card\_Usage;



* Query 8

SELECT 

&nbsp;   CASE 

&nbsp;       WHEN Age BETWEEN 20 AND 30 THEN '20-30'

&nbsp;       WHEN Age BETWEEN 31 AND 40 THEN '31-40'

&nbsp;       WHEN Age BETWEEN 41 AND 50 THEN '41-50'

&nbsp;       ELSE '51+'

&nbsp;   END AS Age\_Group,

&nbsp;   SUM(Personal\_Loan) AS Loan\_Takers,

&nbsp;   ROUND(SUM(Personal\_Loan) \* 100.0 / COUNT(\*), 2) AS Loan\_Acceptance\_Rate\_Percent

FROM 

&nbsp;   Bank\_Personal\_Loan\_Modelling

GROUP BY 

&nbsp;   Age\_Group

ORDER BY 

&nbsp;   Age\_Group;



* Query 9

SELECT 

&nbsp;   CASE 

&nbsp;       WHEN Education=1 THEN 'Undergraduate'

&nbsp;       WHEN Education=2 THEN 'PostGraduate'

&nbsp;     ELSE 'Professional'

&nbsp;   END AS Education\_Level,

&nbsp;   SUM(Personal\_Loan) AS Loan\_Takers,

&nbsp;   ROUND(SUM(Personal\_Loan)\*100.0/COUNT(\*), 2) AS Loan\_Acceptance\_Rate\_Percent

FROM 

&nbsp;   Bank\_Personal\_Loan\_Modelling

GROUP BY 

&nbsp;   Education\_Level

ORDER BY 

&nbsp;   Education\_Level;



* Query 10

SELECT 

&nbsp;   CASE 

&nbsp;       WHEN Online = 1 THEN 'Online User'

&nbsp;       ELSE 'Offline User'

&nbsp;   END AS Online\_Usage,

&nbsp;   SUM(Personal\_Loan) AS Loan\_Takers,

&nbsp;   ROUND(SUM(Personal\_Loan) \* 100.0 / COUNT(\*), 2) AS Loan\_Acceptance\_Rate\_Percent

FROM 

&nbsp;   Bank\_Personal\_Loan\_Modelling

GROUP BY 

&nbsp;   Online\_Usage

ORDER BY 

&nbsp;   Online\_Usage;



