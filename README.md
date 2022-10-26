# LeetCode-SQL-problems
Problems on Leetcode I solved to brush up my SQL! <br>
<b></b>
<b>(https://leetcode.com/problems/customers-who-never-order/description/)[1. Customers Who Never Order]</b><br>
select name as Customers
from customers c --join orders o on c.id = o.customerid
where c.id not in (select customerid from orders)
