<h4> Case Expressions </h4>

declare<br>
&nbsp;&nbsp;&nbsp;&nbsp;v_job_code varchar2(10) := 'Specialist';<br>
&nbsp;&nbsp;&nbsp;&nbsp;v_salary_increase number;<br>
begin<br>
&nbsp;&nbsp;&nbsp;&nbsp;v_salary_increase := <b>case</b> v_job_code<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**when** 'Basic_tech' **then** 0.4<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**when** 'Specialist' 
**then** 0.5<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**else** '0'<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;end;<br>
&nbsp;&nbsp;&nbsp;&nbsp;dbms_output.put_line('Your salary increase is: 
''|| v_salary_increase;<br>
end;

_Will return:_ Your salary increase is: .5

***

declare<br>
&nbsp;&nbsp;&nbsp;&nbsp;v_job_code varchar2(10) := 'Specialist';<br>
&nbsp;&nbsp;&nbsp;&nbsp;v_salary_increase number;<br>
begin<br>
&nbsp;&nbsp;&nbsp;&nbsp;v_salary_increase := <b>case</b> <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**when** v_job_code = 
'Basic_tech' **then** 0.4<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**when** v_job_code in 
('Specialist', 'Supervisor')
**then** 0.5<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**else** '0'<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;end;<br>
&nbsp;&nbsp;&nbsp;&nbsp;dbms_output.put_line('Your salary increase is:
''|| v_salary_increase;<br>
end;

_Will return:_ Your salary increase is: .5