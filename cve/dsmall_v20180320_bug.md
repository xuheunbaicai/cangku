dsmall

dsmall v20180320 bug

    [Suggested description]
    dsmall_v20180320 Delivery address only limits the number of input characters, not sensitive to the character, the available BURP SUITE capture bypassing write XSS statements


    [Additional Information]
    The vulnerability was discovered by downloading the program's source code to local and online deployment tests.

    Location :
    public/index.php/home/memberaddress/index.html

    Code :
    Write with conspicuous characters at the street address, submit, intercept with burp, replace characters with POC, submit, and cause XSS

    Harm:
    An attacker can insert arbitrary HTML/JavaScript code to the page, users can access the information session cookie, user access to the URL, the user's browser and operating system version, can be inserted into the fake login page for fishing, can be linked using a browser vulnerability.

    Conditions for Execution :
    Normal access can

    Edition :
    dsmall_v20180320

    Cause the cause :
    Unfiltered sensitive characters, character input restrictions
    
    POC :
    </td><script>alert(/xss/)</script>

    fix suggestions :
    In the client and server, the data received by the program is fully filtered, and the common dangerous characters for filtering are as follows

    [VulnerabilityType Other]
    Storage type XSS

    [Vendor of Product]
    dsmall

    [Affected Product Code Base]
    dsmall_v20180320

    [Affected Component]
    Delivery address only limits the number of input characters, not sensitive to the character, the available BURP SUITE capture bypassing write XSS statements
    
    [Attack Type]
    Remote

    [Impact Information Disclosure]
    true

    [Attack Vectors] The vulnerability is triggered by accessing the following URL : 
    http://localhost/xuehun/dsmall/public/index.php/home/memberaddress/edit/address_id/2.html

    [Discoverer]
    xuehun
