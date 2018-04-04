

魔方动力

魔方动力 Latest_version bug

[Suggested description] 
The unfiltered CMS search box causes the reflection of the XSS to exist, and the direct output load is popped out

[Additional Information] 
The vulnerability was discovered by downloading the program's source code to local and online deployment tests.

Location : 
product.aspx?q=xuehun" accesskey="X" onclick="alert(document.domain)

Code : 
In the main page search box, enter XSS statements, submissions, pop-up windows

Harm: 
The main page search box does not filter sensitive characters completely, resulting in the execution of XSS statements.

Conditions for Execution : 
Normal access can

Edition :
魔方动力_Latest_version

Cause the cause : 
Unfiltered sensitive characters, character input restrictions

POC : 
xuehun" accesskey="X" onclick="alert(document.domain)

fix suggestions : 
In the client and server, the data received by the program is fully filtered, and the common dangerous characters for filtering are as follows

[VulnerabilityType Other] 
Reflective XSS

[Vendor of Product] 
魔方动力

[Affected Product Code Base]
魔方动力_Latest_version

[Affected Component]
The unfiltered CMS search box causes the reflection of the XSS to exist, and the direct output load is popped out

[Attack Type] 
Remote

[Impact Information Disclosure]
true

[Attack Vectors] The vulnerability is triggered by accessing the following URL : http://127.0.0.1/xuehun/dsmall/public/index.php/home/predeposit/index.html?pdr_sn=%22+accesskey%3D%22X%22+onclick%3D%22alert%28xss%29

[Discoverer] AiLeal

