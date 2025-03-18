<h4> Bind Variables </h4>
Bind variables are variables that are declared but the value is not 
assigned until later in the code.<br>

Ex:<br>

variable var_text varchar2(30);<br>

Notice the line terminator ; appears before a value is assigned := to this 
variable.<br>

***
<h4> Assigning value </h4>
Value is assigned using a : before the variable name and assigning 
value with :=.<br>
<br>
Ex:<br> 

variable var_text varchar2(30);<br>
BEGIN<br>
&nbsp;&nbsp;&nbsp;&nbsp;:var_text := 'Hello PL/SQL';<br>
END; 