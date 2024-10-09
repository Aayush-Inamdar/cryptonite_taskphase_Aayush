# File Globbing
## Matching with *
'*' is treated as a wildcard. The * matches any part of the filename except for / or a leading '.' character.
> cd /ch*
>
> /challenge/run

## Matching with ?
'?' matches exact number of characters as number of times ? is entered. Based on the requirements 
>cd /?ha??enge

## Matching with []
Instructions were pretty clear. All I did was cd to /c*/f* and
>/challenge/run file_[bash]

## Matching path with []
> /challenge/run /challenge/files/file_[bash]

## Mixing Globs
This was quite a tricky challenge. After many permutations and combinations I found the solution to this as
> cd /challenge/files
> /challenge/run ???[*]

## Exlusionary globbing
Similar to previous challenges just
>/challenge/run [!pwn]*

