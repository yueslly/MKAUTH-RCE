# MKAUTH-RCE
An Remote Code Execution on MKAUTH

##Mk-Auth RCE in Central/Suporte/FaleConosco bypassing a .php upload file restriction

##Product Description:
Mk-Auth is a Brazilian Management System for Internet Service Providers used to control client access and permissions via a web interface panel.

##Vulnerability Description:
It is possible bypass a upload file restriction, uploading a .php file that guarantees remote code execution (RCE) accessing the .php file uploaded.

##Additional Information:
Is possible for an authenticated user to upload a .php file and get a remote code execution (RCE). After upload the file, the user need to bruteforce the prefix of the name file, for example, if the user upload the file foo.php123png the name of the file into the system will be af32g44r3f980_foo.php123png so the attacker need to use a tool to brute the prefix to gain access to the file and get the (RCE).

the path to access the file is:

https://{{HOST}}/mkfiles/{{FILE_UPLOADED}}

##Vulnerability Type:
portswigger: https://portswigger.net/web-security/access-control/idor
CWE-434: Unrestricted Upload of File with Dangerous Type

##Vendor:
Mk-Auth

##Affected Product:
MK-AUTH 23.01K4.9
Probably previous are also affected

##Affected Component:
Central: Suporte: Fale Conosco

##Attack Vector:
Remote

##Code Execution:
Yes

##Attack Vector:
An authenticated user must access the .php file uploaded.

##Reference:
	http://mk-auth.com.br/

##Discoverer:
Yueslly Lisboa (0xC4CTU$) | yuesllylisboa[at]gmail.com.br

##Thanks to:
Alan Lacerda (alacerda) | alacerda@intruderlabs.com.br
Filipe Cordeiro (SK) | fsantos@intruderlabs.com.br
All members of intruderLabs <3
