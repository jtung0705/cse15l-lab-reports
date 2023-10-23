# cd commands
> cd (no arguments)

```
[user@sahara ~/lecture1/messages]$ cd
[user@sahara ~]$ 
```
working directory was /home/lecture1/messages

after running became /home/

I got the output because if you type ``cd`` without any parameters, I believe it would go to the home directory. This output is not an error. 
> cd directory

```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$
 ```
working directory was /home/

after running was /home/lecture1

I got this output because if you type ``cd [directory]``, it will change to the directory you mentioned in the command. Not an error.
> cd file

```
[user@sahara ~/lecture1/messages]$ cd zh-cn.txt
bash: cd: zh-cn.txt: Not a directory
```
working directory is /home/lecture1/messages

after at /home/lecture1/messages

I got this output because if you type ``cd [file]``, you cannot change directory to a file. The error is because it is not a directory.

-------------------

# ls commands
> ls (no arguments)

```
[user@sahara ~/lecture1/messages]$ ls
en-us.txt  es-mx.txt  fr-ca.txt  zh-cn.txt
```
working directory before: /home/lecture1/messages

working directory after running command: /home/lecture1/messages

I get this because if you type ``ls``, you just get what file names and sub directories names is in the current directory (but not what is inside the subdirectories), even if the sub directories have or don't have files. Not an error.

> ls directory

```
[user@sahara ~]$ ls lecture1/messages
en-us.txt  es-mx.txt  fr-ca.txt  zh-cn.txt
```
working directory before: /home

working directory after running command: /home

I get this because it just lists whatever files and sub-directories are in the directory you gave as a parameter. Not an error since there are only txt files.
> ls file

```
[user@sahara ~/lecture1/messages]$ ls en-us.txt
en-us.txt
```
working directory before: /home/lecture1/messages

working directory after running command: /home/lecture1/messages

It just shows the file name again, nothing else. Not an error.

---------------

# cat commands
> cat (no arguments)

```
[user@sahara ~/lecture1/messages]$ cat

```
working directory before: /home/lecture1/messages

working directory after running command: /home/lecture1/messages

This just took me out of home directory, no problems. I used Ctrl + C to exit the mode since it interrupts. The ``cat`` command was waiting for an input because its meant to concatenate so that is why when you type again, it outputs the same string because you are concatening a empty string with the string you typed

> cat directory

```
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory
```
working directory before: /home

working directory after running command: /home

This returns an error because you can only use cat to show the contents of a file (like if it was a txt file, it shows the text). The error is that it tells you it is a
directory.

> cat file

```
[user@sahara ~/lecture1/messages]$ cat en-us.txt
Hello World!
```
working directory before: /home/lecture1/messages

working directory after running command: /home/lecture1/messages

This shows me what is inside a file, in this case the en-us.txt contains "Hello World!". No error.
 
