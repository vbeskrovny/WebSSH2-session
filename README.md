# WebSSH2-session
WebSSH2 per-session authentication patches

Here are quick and dirty modifications for the original WebSSH2 node application. They allows to re-request the authentication each time you do a new request for an SSH session. Useful on the jumphosts where you have to use different credentials for the different hosts.


Bear in mind that I'm a network enigneer (cisco professional) and not a programmer, therefore no obligations for the provided code :)))


How to use:
- app.js.patch, expressOptions.js.patch, socket.js.patch, util.js.patch files goes into server directory
- client.html.patch and js.cookie.js files goes into client/public directory
- execute the following command against every file with .patch extension: patch < ./filename.patch
- start/restart the application


Features:
- the last used username/password kept as default and will be re-used for the new hosts
- if authentication method is not accepted - you will be prompted to enter username/password again via "LOGOUT" button on the bottom of the console


Tested:
- Chrome/Firefox



All the best!
