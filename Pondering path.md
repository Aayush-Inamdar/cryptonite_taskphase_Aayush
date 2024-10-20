# Pondering Path
### The Path Variable
In this challenge the command /challenge/run if processed would access the PATH variable and use the rm command stored in it to delete the flag. So I had to change the contents of the path variable making sure rm command cannot be accessed by /challenge/run. I did that by PATH="" which basically wiped out everything

That got me the flag 

pwn.college{kmuzIkVmgfiQzIyNLxWEABwq7Nr.dZzNwUDLzQDO0czW}
### Setting Path
New commands can be created by adding command files to the path variable. Here win was such a command whose command file was /challenge/more_commands. /challenge/run would execute the win command. Since /challenge/run didn't need anything else from PATH I could simply rewrite PATH as /challenge/more_commands. Then I ran /challenge/run which gave me the flag

pwn.college{UxwDmC0xO7RwPI7pP943xeDnQ-O.dVzNyUDLzQDO0czW}
### Adding Commands
I made a sh file win.sh which contained the bash command and cat flag. then I changed its permissions to a=rwx...ie everybody can access it. Then I changed the PATH variable to location of win.sh and then did /challenge/run. This gave me the flag.

pwn.college{gsT5Mghn0oipzRSDustQSg5RNOn.dZzNyUDLzQDO0czW}
### Hijacking Commands
