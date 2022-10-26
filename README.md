# LeetCode-SQL-problems
Problems on Leetcode I solved to brush up my SQL! <br>
<b></b>
<b>[1. Customers Who Never Order](https://leetcode.com/problems/customers-who-never-order/description/)</b><br>
select name as Customers<br>
from customers c<br>
where c.id not in (select customerid from orders)<br>

<b>[2. Calculate Special Bonus](https://leetcode.com/problems/calculate-special-bonus/description/)</b><br>
select employee_id, <br>
case<br>
    when employee_id%2 != 0 and name not like 'M%' then salary<br>
    else 0<br>
    end as bonus<br>
from employees order by employee_id<br>

<b>[3. Second Highest Salary](https://leetcode.com/problems/second-highest-salary/description/)</b><br>
with second_cte as (select salary, dense_rank() over(order by salary desc) rn <br>
from employee)<br>
select max(case when rn=2 then salary else null end) as SecondHighestSalary <br>
from second_cte<br>

