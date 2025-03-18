<h4>Scope</h4>
<br>
In general, variables declared in an outer loop can be accessed or 
called in inner loops. However, variables declared in an inner loop 
cannot be 
accessed in 
an outer loop.<br>

The exception to this is if you use an alias to identify the variables.

Ex:<br>

BEGIN << outer >><br>
&nbsp;&nbsp;&nbsp;&nbsp;DECLARE<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;v_text VARCHAR2(20) := 
'This is an outer variable.'<br>
&nbsp;&nbsp;&nbsp;&nbsp;BEGIN<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;v_text VARCHAR2(20) 
:= 'This is an inner variable of the same name.'<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
BEGIN<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
dbms_output.put_line(v_text);<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
dbms_output.put_line(outer.v_text);<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
END;<br>
&nbsp;&nbsp;&nbsp;&nbsp;END;<br>
END outer;