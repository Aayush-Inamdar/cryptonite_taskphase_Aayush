# Perceiving Permissions
### Changing File Ownership
The chown command can be used to change ownership. To access the /flag file I will have to have the ownership. So I will have to take it from the root. Hence I do chown hacker /flag. Now that I have the ownership all I have to do is cat/flag

pwn.college{Icq1DsUYw0OsHrjd21gMeruHlvw.dFTM2QDLzQDO0czW}
### Groups and files
Similar to chown chgrp command can be used to change the group which has access to an particular file. I had to get myself(hacker) in the group to access the /flag file. So I did chgrp hacker /flag.

This got me access and then all I had to do was cat /flag.

pwn.college{8BXH02Uy8VC0cPxtgeBrT6BK5dO.dFzNyUDLzQDO0czW}
### Fun with Groups Names
The name of my group through which I need to access the /flag need not necessarily be hacker. It can be different. For that I used the id ccommand to check which all groups I am in. Then I do chgrp grpname /flag to get access to/flag. And then I do cat flag.

pwn.college{0fKrgipdtRhzOlW0WfZStCNUJLg.dJzNyUDLzQDO0czW}
### Changing Permissions
Here I know I have to change the permission of /flag file. I tried to change group of /flag file to hacker which was not allowed. Now hacker is neither a root user nor in a group that hass access to it. So permissions for 'other users' need to be changed. Hence I made use of chmod o+rwx /flag

Now I have permission and I cat it for the flag

pwn.college{4kQcJaUVeSNKqahA14kwVHlgL7v.dNzNyUDLzQDO0czW}
### Executable Files
In this challenge I didnt really know If I was in the group or an other user. So I did a+rwx which gave everybody permission to do everything with the file. Now I could run /hallenge/run to get the flag.

pwn.college{YMUSlYOw0BIYcu2B3qKMqazoouA.dJTM2QDLzQDO0czW}
### Permission Tweaking Practice
This was a series of changing permissions where I had to use u,g,o,a and +,- as well as r,w,x intermitently. 

Final flag = pwn.college{Q-7XtH_khmNOr_xTwQyMq0Fzbjw.dBTM2QDLzQDO0czW}
### Permissions Setting practice
This was a series of changing permissions where I had to use u,g,o,a and =,- as well as r,w,x intermitently

pwn.college{oGiZiNnW0Ij6-kCVTjlObAF7AOs.dNTM2QDLzQDO0czW}
### The SUID Bit
I added the SUID bit to the process /challnge/getroot. This gave me access to run /challenge/getroot. Once I got to be the root, I could directly cat the flag.

pwn.college{oGiZiNnW0Ij6-kCVTjlObAF7AOs.dNTM2QDLzQDO0czW}
