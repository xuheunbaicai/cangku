

dsmall

dsmall v20180320 bug

[Suggested description]
Unfiltered CMS main page search box leads to the existence of reflective XSS，Direct output payload pop-up

[Additional Information]
The vulnerability was discovered by downloading the program's source code to local and online deployment tests.

Location :
public/index.php/home

Code :
In the main page search box, enter XSS statements, submissions, pop-up windows

Harm:
An attacker can insert arbitrary HTML/JavaScript code to the page, users can access the information session cookie, user access to the URL, the user's browser and operating system version, can be inserted into the fake login page for fishing, can be linked using a browser vulnerability.

Conditions for Execution :
Normal access can

Edition :
dsmall_v20180320

Cause the cause :
Unfiltered sensitive characters, character input restrictions

POC :
"></a><script>alert(/xss/)</script>

fix suggestions :
In the client and server, the data received by the program is fully filtered, and the common dangerous characters for filtering are as follows

[VulnerabilityType Other]
Reflective XSS

[Vendor of Product]
dsmall

[Affected Product Code Base]
dsmall_v20180320

[Affected Component]
Unfiltered CMS main page search box leads to the existence of reflective XSS，Direct output payload pop-up

[Attack Type]
Remote

[Impact Information Disclosure]
true

[Attack Vectors] The vulnerability is triggered by accessing the following URL : 
http://127.0.0.1/xuehun/dsmall/public/index.php/home

[Discoverer]
xuehun

