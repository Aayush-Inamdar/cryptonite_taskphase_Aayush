# Process and Jobs
### Listing Processes
It is told that I cant ls /challenge but the process is running. So I have to look into running processes to find the Flag containing processes.

So I do ps -ef to find a running process /challenge/13790-run-7083. I launch this process to get the flag

pwn.college{MS5kljbfa9SsFvZJAHpjC9xwwm9.dhzM4QDLzQDO0czW}
### Killing Processes
I had to find PID of /challenge/dont_run so I did ps -ef. Then I killed the process by doing kill 73 (the PID) and then did/challenge/run for the flag

pwn.college{I1DM9fzF9c0Y2hz5w4sGrBotTms.dJDN4QDLzQDO0czW}
### Interrupting Processes
Ctrl-C is a type of Interrupt. Some processes cannot run without it. So when /challenge/run didn't execute by itself, I pressed Ctrl-C and got the flag.

pwn.college{gkyhldEktjOoZnVqnMPL86UFjC5.dNDN4QDLzQDO0czW}
### Suspending Processes
Ctrl-Z is a way to push a process behind another process instead of totally terminating it. The challenge needed one challenge/run in the background and one up front so I did 
> /challenge/run
>
> Ctrl-Z
>
> /challenge/run

This gave the flag

pwn.college{AzTjoAPXsxhe5bwSG6vm0S5ZKA-.dVDN4QDLzQDO0czW}
### Resuming Processes
Any process which has been temporarily suspended can be brought back by using the fg builtin. So I first ran /challenge/run suspended it by Ctrl-Z then brought it back by fg /challenge/run to get the flag.

pwn.college{0-tDzNIbUnVbrA_pUEaL1bxdt6b.dZDN4QDLzQDO0czW}
### Backgrounding Processes
When you suspend a process it doesnt terminate but still it stops. The bg builtin allows it to run in background allowing us to run another command in the foreground. This is what I did.
> /challenge/run
>
> Ctrl-Z (Now the process is suspended)
>
> bg /challenge/run (Now it is running in the background)
>
> /challenge/run ( Now it fill find a copy of the process running in the background and give me the flag)

pwn.college{QMTRlOnkZLua8Rey83xb2sZ2UuC.ddDN4QDLzQDO0czW}
### Foregrounding Processes
First I ran /challenge/run then suspended it by Ctrl Z then got it running in the background by bg and then again brought it to the foreground by fg

pwn.college{AXF5ONUln2wEvmB7I7NNF7DN772.dhDN4QDLzQDO0czW}
### Starting Backgrounded Processes
No need to do CTRL Z then bg...we can directly do /challenge/run &

pwn.college{w_s8VgsEQV5dZOrC6TwSlADL2vN.dlDN4QDLzQDO0czW}
### Process exit codes
Using $? gives the exit code for a process. I had to get exit code of /challenge/get-code process which was 23. The I had to pass 23 as an arguement to /challenge/submit-code 23. This got me the flag

pwn.college{8CslhZ-Slpw4VBEuZe3bGSLUxAL.dljN4UDLzQDO0czW}
