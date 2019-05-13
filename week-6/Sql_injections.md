# Script injections / Safety issues

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQueA5_SqiIayEOW47gQiKmlhwyAUc5iDMUsGk512xyZnFqhVpr8w)

## 1) What is a script injection and how do these happen?  
Javascript can be used not only for good purposes but for some malicious attacks too. One among that is Javascript Injection. The essence of JS Injection is to inject the Javascript code, that will be run from the client-side. Script injection is security vulnerability, a serious security threat that enables an attacker to inject malicious code in the user interface elements of your Web form of data-driven Web sites.   

The following are some of the most common HTML tags that may be prone to script injection attacks:  
script / meta / html / body / embed / frame /   frameset / img / style / link / object  

![](https://vpit.rice.edu/sites/g/files/bxs1381/f/sorted-XSS_0.png)

## 2) How would you prevent script injections?
Here are some techniques you can adopt to avoid script injection attacks in your applications:

1. You can disable request validation in your Web page.

2. Using Server.HTMLEncode() to encode the user's input

   String strName = Server.HtmlEncode(TextBox1.Text);

 Response.Write("Name: "+strName);

3. Rejecting certain special characters like, "<", ">", "=", "%", "!", "@", etc.

4. Ensuring the correct data is entered in the Web form user interface elements before the form is submitted. Also, you should restrict the user's input to a certain type and number of characters. As an example, if you are accepting a name from a user, it should only contain alphabets, spaces, and dots. You should not allow the user to type in other characters and then submit the input.     




### Another common form of injection attack is SQL Injection:  


![](https://www.itdominator.com/wp-content/uploads/2018/03/sqlInjection.png)  


SQL injection is a code injection technique that might destroy your database.  
SQL injection is one of the most common web hacking techniques.  
SQL injection is the placement of malicious code in SQL statements, via web page input.

SQL injection usually occurs when you ask a user for input, like their username/userid, and instead of a name/id, the user gives you an SQL statement that you will unknowingly run on your database.

SQL Injection Based on Batched SQL Statements
Most databases support batched SQL statement.

A batch of SQL statements is a group of two or more SQL statements, separated by semicolons.

The SQL statement below will return all rows from the "Users" table, then delete the "Suppliers" table.

### **Example:**  

**code:**  
````
txtUserId = getRequestString("UserId");
txtSQL = "SELECT * FROM Users WHERE UserId = " + txtUserId;
````

**Input:**
````
User id:
105; DROP TABLE Suppliers
````

** The valid SQL statement would look like this: **

````
SELECT * FROM Users WHERE UserId = 105; DROP TABLE Suppliers; ````
