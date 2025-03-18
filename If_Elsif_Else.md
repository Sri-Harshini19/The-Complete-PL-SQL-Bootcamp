<h4> Control Structures </h4>

The code blocks that change the path of a running program.<br>

Ex. Loops, If Statements, Case Statements
***

DECLARE<br>
&nbsp;&nbsp;&nbsp;&nbsp;v_number number := 30;<br>
BEGIN<br>
&nbsp;&nbsp;&nbsp;&nbsp;<b>if</b> v_number < 20 then<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;dbms_output.put_line('Less than 20')
;<br>
&nbsp;&nbsp;&nbsp;&nbsp;<b>elsif</b> v_number < 30 then<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; dbms_output.put_line('Less than 
30');<br>
&nbsp;&nbsp;&nbsp;&nbsp;<b>else</b><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;dbms_output.put_line('30 or greater.
');<br>
END;<br>

Will print: _30 or greater._