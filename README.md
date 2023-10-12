# urltools


POSIX shellscripts for dealing with urls:

* `urlgrep` : Extract url-like strings from text
* `urlencode` : Percent-encode strings or files
* `urldecode` : Percent-decode strings or files


## Usage examples

Extract all urls from the `bash(1)` manpage
```
$ man -P cat bash | urlgrep
http://pubs.opengroup.org/onlinepubs/9699919799/
http://tiswww.case.edu/~chet/bash/POSIX
ftp://ftp.gnu.org/pub/gnu/bash/
```

Percent-encode and decode strings or files
```
# String as a parameter
$ urlencode €
%E2%82%AC

# String from stdin
$ printf '%s' 'https://github.com/jaf7C7' | urlencode | tee file
https%3A%2F%2Fgithub.com%2Fjaf7C7

# String from file
$ urldecode file
https://github.com/jaf7C7
```
