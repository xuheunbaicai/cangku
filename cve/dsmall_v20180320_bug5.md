

dsmall

dsmall v20180320 bug

[Suggested description] 
The unfiltered CMS search box causes the reflection of the XSS to exist, and the direct output load is popped out

[Additional Information] 
The vulnerability was discovered by downloading the program's source code to local and online deployment tests.

Location : 
public/index.php/home/predeposit/index.html?pdr_sn="+accesskey%3D"X"+onclick%3D"alert(xss)

Code : 
In the main page search box, enter XSS statements, submissions, pop-up windows

Harm: 
After login, the personal page, recharge the single number search box, unfiltered sensitive character, cause XSS


Conditions for Execution : 
Normal access can

Edition : 
dsmall_v20180320

Cause the cause : 
Unfiltered sensitive characters, character input restrictions

POC : 
" accesskey="X" onclick="alert(xss)

fix suggestions : 
In the client and server, the data received by the program is fully filtered, and the common dangerous characters for filtering are as follows

[VulnerabilityType Other] 
Reflective XSS

[Vendor of Product] 
dsmall

[Affected Product Code Base] 
dsmall_v20180320

[Affected Component] 
The unfiltered CMS search box causes the reflection of the XSS to exist, and the direct output load is popped out

[Attack Type] 
Remote

[Impact Information Disclosure] 
true

[Attack Vectors] The vulnerability is triggered by accessing the following URL : 
http://127.0.0.1/xuehun/dsmall/public/index.php/home/predeposit/index.html?pdr_sn=%22+accesskey%3D%22X%22+onclick%3D%22alert%28xss%29

[Discoverer] AiLeal
