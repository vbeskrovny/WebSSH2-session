# WebSSH2-session
WebSSH2 per-session authentication patches

<img src="https://raw.githubusercontent.com/vbeskrovny/WebSSH2-session/master/login.png">
<img src="https://raw.githubusercontent.com/vbeskrovny/WebSSH2-session/master/login2.png">

Here are quick and dirty modifications for the original WebSSH2 node application. They allows to re-request the authentication each time you do a new request for an SSH session. Useful on the jumphosts where you have to use different credentials for the different hosts.


Bear in mind that I'm a network enigneer (cisco professional) and not a programmer, therefore no obligations for the provided code :)))


How to use:
- app.js.patch, expressOptions.js.patch, socket.js.patch, util.js.patch files goes into server directory
- client.html.patch, webssh2.bundle.js.patch login.css and js.cookie.js files goes into client/public directory
- execute the following command against every file with .patch extension: patch < ./filename.patch
- start/restart the application


Features:
- the last used username/password kept as default and will be re-used for the new hosts
- any hostname as param is accepted now (I am using custom FQDN scheme, therefore validator was not accepting it before)
- if authentication method is not accepted - you will be prompted to enter username/password again
- hostname is on the title now, so the page can be bookmarked
- logout / login / close buttons added


Tested:
- Chrome/Firefox



All the best!
