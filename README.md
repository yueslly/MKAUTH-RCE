# MKAUTH-RCE
An Remote Code Execution on MKAUTH

##Mk-Auth RCE in Central/Suporte/FaleConosco bypassing a .php upload file restriction

##Product Description:
Mk-Auth is a Brazilian Management System for Internet Service Providers used to control client access and permissions via a web interface panel.

##Vulnerability Description:
It is possible to bypass an upload file restriction, by uploading a .php file that guarantees remote code execution (RCE) accessing the .php file uploaded.

##Additional Information:
An authenticated user can upload a .php file and get a remote code execution (RCE). After uploading the file, the user needs to brute force the prefix of the name file, for example, if the user uploads the file foo.phpJunk123png the name of the file into the system will be af32g44r3f980_foo.phpJunk123png so the attacker needs to use a tool to brute force the prefix to gain access to the file and get the (RCE).

the path to access the file is:

https://{{HOST}}/mkfiles/{{FILE_UPLOADED}}

Note: To bypass the upload file restriction you need to use the suffix ".phpJunk123png", it will be uploaded and interpreted by the system.

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

##Code Execution:
Yes

##Attack Vector:
Remote -- An authenticated user must access the .php file uploaded to gain remote code execution (RCE).

##Reference:
	http://mk-auth.com.br/

##Discoverer:
Yueslly Lisboa (0xC4CTU$) | yuesllylisboa[at]gmail.com.br

##Thanks to:
Alan Lacerda (alacerda) | alacerda@intruderlabs.com.br
All members of intruderLabs <3
and Filipe C. (SK)
