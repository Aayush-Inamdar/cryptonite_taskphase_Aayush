# Untangling Users
### Becoming root with Su
This challenge was fairly simple I put in the su command the password and catted the flag

pwn.college{UifItOfezapn3DIcBGjOKbKcOEl.dVTN0UDLzQDO0czW}
### Other users with su
In this challenge we had to add an attribute to su 'zardus' to become that particular user and not root in general. running /challenge/run got me the flag.

pwn.college{Q15Ze-nOHivrgXTpKt89m4VDp8Y.dZTN0UDLzQDO0czW}
### Cracking Passwords
First I had to use /challenge/shadow-leak as john which I did by john /challenge/shadow-leak

THen that gave me a password 'aardvark' So I did su zardus, put in the password and became zardus
then I run /challenge/run to get the flag

pwn.college{UWc5GvLrDYUYMrzjUPSZtOpqbJC.ddTN0UDLzQDO0czW}
### Using sudo
When I type sudo, i temporarily become the root. So all I had to do was sudo cat /flag

pwn.college{wMpohyxzqVHOFlwKxSEdiG1QkS1.dhTN0UDLzQDO0czW}
