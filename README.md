# LeetCode-SQL-problems
Problems on Leetcode I solved to brush up my SQL! <br>
<b></b>
<b>[1. Customers Who Never Order](https://leetcode.com/problems/customers-who-never-order/description/)</b><br>
select name as Customers<br>
from customers c<br>
where c.id not in (select customerid from orders)<br>
