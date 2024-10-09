# Practicing Piping
Using redirection codes can be made much shorter and faster. In this module I learned how to redirect my input and output directly to other commands.
## Redirecting output
> echo PWN > COLLEGE
>
> /challenge/run > myflag

## Appending 
> /challenge/run >> /home/hacker/the-flag
>
> cat /home/hacker/the-flag

## Redirecting Errors
FD 0: Standard Input

FD 1: Standard Output

FD 2: Standard Error

In this challenge two arguements had to be given
> /challenge/run 1> myflag 2> instructions

## Redirecting Input
> echo COLLEGE > PWN
>
> /challenge/run < PWN

## Grepping live output
| is called the pipe operator. Using this we dont need to print the output to the terminal and multiple steps can be saved
> /challenge/run | grep pwn.college /challenge/run

## Grepping errors
| operator usually pipes only the output. If we want to redirect the input we will have to use a special operator >&. In this case since we want to send input over to the other side we do 2>&1.
> /challenge/run 2>&1 | grep pwn.college /challenge/run

## tee
Piping helps in avvoiding saving output to files but that causes problems as we may not know where exactly the code went wrong. for that the tee operator is available. It copies the output and stores it to a file as well as redirects it to the other command
> /challenge/pwn | tee PWN | /challenge/college
>
> cat PWN
>
> /challenge/college --secret CODE

The PWN file contained the output of /challenge/pwn which was the secret arguement that needed to be passed to the /college program.

## writing to multiple programs
> /challenge/hack | tee >(/challenge/the) >(/challenge/planet)

## Split piping stderr and stdout
Needed help of ChatGPT for this one
> /challenge/hack > >( /challenge/planet ) 2> >( /challenge/the )
