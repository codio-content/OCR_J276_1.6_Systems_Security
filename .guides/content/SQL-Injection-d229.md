## The concept of SQL injection 
SQL(Structured Query language) is a programming language used to manipulate a database. If a network or website involves the use of a database then a hacker could interact with it for a malicious purpose. Most websites allow a user to enter input e.g. username and password, however in most cases there is no validation to not accept anything else. For example a hacker could write his own SQL Query that could be sent to the database via the input box and the whole database could be stolen.

Consider this example:

A normal piece of SQL Pseudocode to lookup a user might look like this:
```
InputUsername=txtUsername

InputPassword=txtPassword

Select * FROM tblUsers WHERE Username=InputUsername AND Password=InputPassword
```
But what if a Hacker entered this into the text box?

```
Select * FROM tblUsers WHERE Username=InputUsername AND Password=InputPassword OR 1=1
```

Now because 1 always equals 1 this condition will be met and all of the users will be returned.