**Employee with most orders**

/\*

&nbsp;\* This query identifies employee who has handled the most orders by grouping 

&nbsp;\* the orders table by employeeid and count the number of orders.

&nbsp;\*/



SELECT 

&nbsp;	CONCAT(e.lastname, ' ', e.firstname) AS Employee,  

&nbsp;	COUNT(o.orderid)  AS Total\_order 

FROM 

&nbsp;	employees e 

INNER JOIN 

&nbsp;	orders o ON e.employeeid = o.employeeid

GROUP BY 

&nbsp;	e.lastname, e.firstname 

ORDER BY 

&nbsp;	Total\_order DESC

