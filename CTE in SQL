--CTE in SQL

with cte_Employee as
(select firstname, lastname, gender,salary
,count(gender) over (partition by gender) as totalgender
,avg (salary) over (partition by gender) as avgsalary
from employeedemographics emp
join employeesalary sal
on emp.employeeid = sal.employeeid
where salary>'45000'
)

select lastname, salary
from cte_Employee
