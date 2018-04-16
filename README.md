# WebSSH2-session
WebSSH2 per-session authentication patches

Here are quick and dirty modifications for the original WebSSH2 node application to allow per-session authentication for your hosts.

Bear in mind that I'm a network enigneer (cisco professional) and not a programmer. Therefore no obligations for the provided code.


How to use:
- app.js.patch, expressOptions.js.patch, socket.js.patch, util.js.patch files goes into server directory
- client.html.patch and js.cookie.js files goes into client/public directory
- execute the following command against every file with .patch extension: patch < ./filename.patch
- start/restart the application


Features:
- the last used username/password kept as default
- if method is not accepted - you will be prompted to enter username/password again


Tested:
- Chrome/Firefox
