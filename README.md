# Lab-Postresql
Serik Bakhramov Lab1 DB
1.
1.Find the Id,name of each employee who works for “BigBank”
Пid ,person_name (Ჾcompany_name=”BigBank”(works))
2.Find the Id, name, city of residence of each employee who works for “BigBank”.
Пemployee.id, employee.person_name,employee.city(Ჾemployee.person_name=works.person_name(Employee x works))
3.Find the id, name, street, city of residence of each employee who works for “BigBank” and earns more than 10000
Пemp.id, emp.person_name, emp.street, emp.city(Ჾemp.person_name=works.person_name ^ works.salary>10000(Employee x works))
4.Find the id, name of each employee this database who lives in the same city as the company for which he works.
Пemp.id, emp.person_name(Ჾemp.person_name=works.person_name ^ works.company_name=company.company_name ^ emp.city=company.city(Employee x works x company))
2.
1.Find the id,name of each employee who doesn’t work for “BigBank”
Пid ,person_name (Ჾcompany_name != ”BigBank”(works))
2.Find the Id,name of each employee who earns at least as much as every employee in the database
Пid, person_name(Ჾsalary>(avg(salary)(works))(works))


