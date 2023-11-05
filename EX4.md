# Ex. No: 4 Creating Procedures using PL/SQL
## DATE :

### AIM : 
To create a procedure using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

### Program:
```
SQL> CREATE TABLE emp(empid NUMBER,empname VARCHAR(10),dept VARCHAR(10),salary NUMBER);
```
```
SQL>  CREATE OR REPLACE PROCEDURE emp_data AS
  2  BEGIN
  3  INSERT INTO emp(empid,empname,dept,salary)values(1,'MOHIT','AIDS',85000
);
  4  INSERT INTO emp(empid,empname,dept,salary)values(1,'LOKESH','CSE',70000
);
  5   INSERT INTO emp(empid,empname,dept,salary)values(1,'SAJAN','IT',75000);
  6  COMMIT;
  7  FOR emp_rec IN (SELECT * FROM emp)LOOP
  8  DBMS_OUTPUT.PUT_LINE('EMPLOYEE ID:'||emp_rec.empid||',EMPLOYEE NAME:'|| emp_rec.empname||',DEPARTMENT:'||emp_rec.dept||',SALARY:'||emp_rec.salary);

  9  END LOOP;
 10  END;
 11  /
```
```
SQL> begin
  2  emp_data;
  3  end;
  4  /
```



### Output:
![Screenshot 2023-10-08 122700](https://github.com/Mamthaiyappaprabu/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/119393563/1c6cc3ee-5293-4081-af11-c509a312b0d0)



### Result:
The output is verified successfully.
