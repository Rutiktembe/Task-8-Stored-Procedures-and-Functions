# Task-8-Stored-Procedures-and-Functions

1.Use CREATE PROCEDURE and CREATE FUNCTION


SQL> CREATE OR REPLACE PROCEDURE IncreaseSalary (
  2      emp_id IN NUMBER,
  3      percentage IN NUMBER
  4  )
  5  IS  
  6  BEGIN
  7      UPDATE Employees
  8      SET Salary = Salary + (Salary * percentage / 100)
  9      WHERE EmpID = emp_id;
 10  
 11      COMMIT;
 12  END;
 13  /

Procedure created.

2.2.Use parameters and conditional logic

SQL> BEGIN
  2      IncreaseSalary(101, 10);
  3  END;
  4  /
  
