<h4> For Loops </h4>

FOR counter IN [lower_bound]..[upper_bound] LOOP<br>
&nbsp;&nbsp;&nbsp;&nbsp;your_code;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;:::::::<br>
END LOOP;
***

begin<br>
&nbsp;&nbsp;&nbsp;&nbsp;for i in 1..3 loop<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;dbms_output.put_line
('My count is : ' || i);<br>
&nbsp;&nbsp;&nbsp;&nbsp;end loop;<br>
end;

_Will print :_ <br>
My count is 1<br>
My count is 2<br>
My count is 3<br>
***

begin<br>
&nbsp;&nbsp;&nbsp;&nbsp;for i in _reverse_ 1..3 loop<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;dbms_output.put_line
('My count is : ' || i);<br>
&nbsp;&nbsp;&nbsp;&nbsp;end loop;<br>
end;

_Will print :_ <br>
My count is 3<br>
My count is 2<br>
My count is 1<br>
