# Comprehending Commands
In this module I learned how to use various basic and necessary commands
### cat
The first challenge was really easy where the flag was in the 'flag' file and all I had to do was
> cat flag

Arguements to cat can also be absolute paths. That was the second challenge. What I did here was
> cat /flag

The third challenge was a bit tricky. I used 'ls' command to check the home directory and used ls and cd till I fount the flag file.
Then I catted out the absolute path and got the flag
### grep
This challenge was pretty easy. Format of the command was already given in the description. All I had to do was
> cat /challenge/data.txt
>
> grep pwn.college /challenge/data.txt
### listing files
In this challenge I just did ls /challenge to find the renamed run file
### touch and remove
Again pretty straight-forward challenges. Used touch and rm to get the flag
### hidden files
On using ls -a it revealed a new file in home directory starting with a '.'. I cat that file and followed further to get the flag
### An Epic Filesystem Quest
This was a very fun challenge that needed a bit of patience. It was basically only an application of all commands I learned till now in this module. In some cases I had to ls cd cat ls-a untill I ultimately found the flag.
### find
The command was specified in the description. So what I did was
> find / -name flag

This genereated many many files to which permission was denied but 5-6 where I had permission. I had to check every one of these. Because I didn't know if these were directories, files or programs I had to try out various combinations of cd, ls, cat or running them till I found the flag
### linking files
In this challenge I created a symlink between /flag and /not-the-flag and catted /challenge/catflag to get me the flag.
> ln -s /flag ~/not-the-flag
>
> cat /challenge/catflag
