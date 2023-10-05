
# cd commands
> cd (no arguments)

```
[user@sahara ~/lecture1/messages]$ cd
[user@sahara ~]$ 
```
I got the output because if you type ``cd`` without any parameters, I believe it would go to the home directory. This output is not an error.
> cd directory

```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$
 ```
I got this output because if you type ``cd [directory]``, it will change directory to the location. Not an error.
> cd file

```
[user@sahara ~/lecture1/messages]$ cd zh-cn.txt
bash: cd: zh-cn.txt: Not a directory
```
I got this output because if you type ``cd [file]``, you cannot change directory to a file. The error is because it is not a directory.

-------------------

# ls commands
> ls (no arguments)

```
[user@sahara ~/lecture1/messages]$ ls
en-us.txt  es-mx.txt  fr-ca.txt  zh-cn.txt
```
I get this because if you type ``ls``, you just get what is in the directory there and it lists it. Not an error.

> ls directory

```
[user@sahara ~]$ ls lecture1/messages
en-us.txt  es-mx.txt  fr-ca.txt  zh-cn.txt
```
I get this because it just lists whatever files are in the directory. Not an error.
> ls file

```
[user@sahara ~/lecture1/messages]$ ls en-us.txt
en-us.txt
```
It just shows the file name again, nothing else. Not an error.

---------------

# cat commands
> cat (no arguments)

```
[user@sahara ~/lecture1/messages]$ cat

```
This just took me out of home directory, no problems.
> cat directory
> 
```
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory
```
This returns an error because you can only use cat to list files. The error is that it tells you it is a directory.
> cat file
```
[user@sahara ~/lecture1/messages]$ cat en-us.txt
Hello World!
```
This shows me what is inside a file, in this case the en-us.txt. No error.

