<h4> While Loops </h4>

WHILE [condition] LOOP<br>
&nbsp;&nbsp;&nbsp;&nbsp;Your code<br>
&nbsp;&nbsp;&nbsp;&nbsp;::::::::<br>
END LOOP
***
declare<br>
&nbsp;&nbsp;&nbsp;&nbsp;v_counter number(2); := 1;<br>
begin<br>
&nbsp;&nbsp;&nbsp;&nbsp;WHILE v_counter <= 10 LOOP<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;dbms_output.put_line('My counter is : '||
v_counter);<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;v_counter :=
v_counter + 1;<br>
&nbsp;&nbsp;&nbsp;&nbsp;END LOOP;<br>
end;