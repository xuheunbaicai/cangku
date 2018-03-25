

dsmall

dsmall v20180320 bug

[Suggested description]
Access to the page, view the page source code, there is a path leak

[Additional Information]
The vulnerability was discovered by downloading the program's source code to local and online deployment tests.

Location :
public/index.php/home/predeposit/index.html?pdr_sn=aaa

Code :
When testing the application, it is found that the application is fault-tolerant, and any attacker can get the error of the program to the absolute path of the site by making the program false.

Harm:
When testing the application, it is found that the application is fault-tolerant, and any attacker can get the error of the program to the absolute path of the site by making the program false.

Conditions for Execution :
Normal access can

Edition :
dsmall_v20180320

Cause the cause :
Non permissions restrictions

POC :
null

fix suggestions :
Non permissions restrictions

[VulnerabilityType Other]
Absolute path leakage

[Vendor of Product]
dsmall

[Affected Product Code Base]
dsmall_v20180320

[Affected Component]
The vulnerability was discovered by downloading the program's source code to local and online deployment tests.

[Attack Type]
Remote

[Impact Information Disclosure]
true

[Attack Vectors] The vulnerability is triggered by accessing the following URL : 
http://127.0.0.1/xuehun/dsmall/public/index.php/home/predeposit/index.html?pdr_sn=aaa

[Discoverer]
xuehun

