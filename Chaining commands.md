# Chaining commands
### Chaining with semicolons
Two commands can be chained together using a semicolon. So I ran /challenge/pwn and /challenge/college together by puting a ; between them.

### First Shell Script
Shell script is a way of combining a set of commands in a file...which usually has a .sh extension. First I had to create such a file for which I used a 'nano' command. The nano command led to to a different shell x.sh wherein I put my commands /challenge/pwn and /challenge/college. Then i pressed Ctrl + X to exit from the shell. After returning to the original shell I put bash x.sh and it gave me the flag.

pwn.college{47PJKdB8yqahU5YvwmuFhqaNemk.dFzN4QDLzQDO0czW}
### Redirecting script output
The first process was same as previous challenge. I had to make a .sh file in which i wrote the /pwn and /college commands. then i did bash script.sh|/challenge/solve...which basically put output of 1st two commands as input of 3rd.

pwn.college{st3jelsYyRpC3Eb43f2z02OnyOl.dhTM5QDLzQDO0czW}
### Executable shell scripts
I did nano abc.sh wrote the /solve in it closed it altered its permissions using chmod and then executed it by ./abc.sh

pwn.college{EZ8o--bnrRkXYxfFymS_hg4ZKKO.dRzNyUDLzQDO0czW}
