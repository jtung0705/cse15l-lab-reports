
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

```
placeholder
```
> cat file

```
placeholder
```

 
For each of the commands cd, ls, and cat, and using the workspace you created in this lab:

Share an example of using the command with no arguments.
Share an exmaple of using the command with a path to a directory as an argument.
Share an example of using the command with a path to a file as an argument.
So that’s 9 total examples (3 for each command). For each, include:

- A screenshot or Markdown code block showing the command and its output
- What the working directory was when the command was run
- A sentence or two explaining why you got that output (e.g. what was in the filesystem, what it meant to have no arguments).
- Indicate whether the output is an error or not, and if it’s an error, explain why it’s an error.

