## Searching commands
* `pwd` - print working directory of where u are in
* `ls` - lists the files & directories inside working directory
* `ls -a` - shows all files and hidden files in pwd 
* `ls -d /usr/include/s*` - shows all files in this path that begines with letter s
* `mount` - lists the name of the file system used
* `locate file` - locates the file 
* `updatedb` - updates the database
* `echo /usr/bin/a*` - finds all files that starts with a in `/usr/bin` and lists them 
* `echo /usr/bin/a??` - finds all files that starts with a and only has 3 characters in `/usr/bin` and lists them 
* `find` - lists all files in current directory
* `find . -name "program.c"` - finds specific file in current directory
*  `find . -name "prog*"` - finds all files starting with prog in current directory
* `find / -name "hello"` - finds a file called hello from the whole system
* `find / -name "hello" 2> /dev/null` - finds a file called hello from the whole system and `redirects error` mesages to a black hole `called null` that doesnt keep it
* `find / -iname "*joe*" 2> /dev/null` - finds all files containing joe `ignoring upper & lower case`
* `find / -ipath "*joe*" 2> /dev/null` - finds all paths containing joe `ignoring upper & lower case, including the directories