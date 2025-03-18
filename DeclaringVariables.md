<h3>Declaring Variables</h3>
Name [CONSTANT] datatype [NOT NULL] [:=|DEFAULT value|expression];<br>

***
<h4> Setting a Default Value </h4>
DECLARE <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;V_TEXT VARCHAR2 (50) NOT NULL DEFAULT 'HELLO'; <br>
BEGIN <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;DBMS_OUTPUT.PUT_LINE(V_TEXT); <br>
END;<br>

Will print: _HELLO_

<h4> Create and initialize method </h4>
DECLARE <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;V_TEXT VARCHAR2 (50) NOT NULL := 
'WELCOME'; <br>
BEGIN <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;DBMS_OUTPUT.PUT_LINE(V_TEXT); <br>
END; <br>

Will print: _WELCOME_
***
<h4> Declaring a Value (other than the default)</h4>
DECLARE <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;V_TEXT VARCHAR2 (50) NOT NULL DEFAULT 'HELLO'; <br>
BEGIN <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;V_TEXT := 'PL/SQL'; <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;DBMS_OUTPUT.PUT_LINE(V_TEXT); <br>
END; <br>

Will print: _PL/SQL_

***
<h4> Concatenate on a Variable '||'</h4>
DECLARE <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;V_TEXT VARCHAR2 (50) NOT NULL DEFAULT 'HELLO'; <br>
BEGIN <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;V_TEXT := 'PL/SQL' || ' Course'; <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;DBMS_OUTPUT.PUT_LINE(V_TEXT || ' 
Beginner to Advanced'); <br>
END; <br>

Will print: _PL/SQL Course Beginner to Advanced_
***
<h4> Numbers </h4>

DECLARE <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;V_NUMBER NUMBER (or PLS_INTEGER) NOT 
NULL := 50.42;<br>
BEGIN <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;DBMS_OUTPUT.PUT_LINE(V_NUMBER);<br>
END;

Will Print: _50.42_
***
<h4> Dates </h4>

DECLARE <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;V_DATE DATE NOT NULL := SYSDATE;<br>
BEGIN <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;DBMS_OUTPUT.PUT_LINE(V_DATE);<br>
END;

Will Print: _dd-mmm-yyyy_ <br>
This format can be changed in Preferences > Database > NLS
***
<h4> Xx Boolean xX </h4>

DECLARE <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;V_BOOL BOOLEAN := TRUE;<br>
BEGIN <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;DBMS_OUTPUT.PUT_LINE(V_BOOL);<br>
END;

_Returns an error because we cannot print Boolean values, we can only 
use them in "if" statements._
***