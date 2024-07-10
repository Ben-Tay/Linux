## Typical File path
> /folder/subfolder/file
* `first /` also known as the root folder
* OS itself has a lot of files to keep track of as well - `utility programs, applications, methods to connect with devices etc`.

## FSSTND (File System Standard)
> File system hierachy standard to GNU Linux

##### `/bin` 
*  directory which contains all of the basic commands needed to start and use a minimal system.
* abbreviation for `binary` as the executable form of an application is in `binary`

##### `/sbin`
* directory which contains all of the commands needed for the `super or root user`
* super user is `aka` the administrator of the computer with more user controls

##### `/home`
* contains all of the `user directories`
* eg: `/home/Smith`

##### `/root`
* Home directory of the `root user`

##### `/etc`
* Directory that contains configuration files
* Abbreviation for `editable text configuration`

##### `/lib`
* Stores software libaries required for executables in `/bin` and `/sbin`

##### `/tmp`
* Used to store temporary files
* Typically located in `/var/tmp` or `/run/tmp`
* Emptied every time you restart the computer

##### `/var`
* Contains various files used by the operating system such as `databases, emailboxes, history` etc
* Eg: `/var/logs` - to show system los

##### `/usr`
* UNIX System Resources
* Contains some subfolders similar to those present in root but `extends the system operations`
* eg: `/usr/bin` contains executables that are not essential to start the system

*  eg: `/usr/lib` contains libaries that are not essential to start the system

##### `/dev`
* Contains file that corresponds, directly or indirectly, to a physical `device`.
* `/dev/printer`
* `/dev/audio`
* `/dev/mem`
* `/dev/network`

### Commands to use in file system
* `cd / ` - change directory to root directory
* `cd ` - cd alone would always bring us to the home user folder
* `cd ./sys` - from curr directory change to sys 
* `cd ../..` - brings us to root directory if we are in `~` (relative path)
* `cd /sys` - absolute path because starts with `/` aka the root
* `file file_name` - displays the file type 
* `realpath file_name` - displays the absolute path of the file
* `which binary_file` - displays the absolute path of binaries


## Creating/Deleting/Reading files

#### Create
* `touch file_1` - creates an empty file w the filename of file 1
* `touch file_1 file_2` - creates 2 empty files
* `touch 'my file'` - creates `my file`

#### Delete
* `rm file_name` - removes that specific file
* `rm file_1 file_2` - removes both files
* `rm 'my file'` - removes `my file`

#### Read
* `cat file_name` - snippet of file contents
* `echo 'hello world' > file2.txt` - redirects the output of the command echo into file2.txt
* `cat file2.txt > file3.txt` - basically copies the contents of file2 into file 3
* `cat > anotherfile.txt` - creates another file and u have to write input in and enter, use ctrl D to indicate end of input

##### Dealing w long files
* `cat /etc/services | more` - pipes the output of the first command `cat` into the input of the `2nd command more`, which shows only the 1st page.
* `cat /etc/services | less` - basically more but with added functionalities like scrolling, `j` to scroll 1 line up, `k` to scroll 1 line down, `g` - beginning, `G`- end of doc
* `more file_name.txt` - does the same above
* `less file_name.txt` - does the same above
* `head /etc/services` - shows the head of the file

#### Searching within less
* `/` - forward search
* `?` - backward search

## Dealing w Directories
* `mkdir folder` - makes a directory called `folder`
* `mkdir f1 f2 f3` - create multiple directories at once
* `mkdir -p D1/D2/D3/D4` - recursively creates subfolders
* `rm -r folder` - recursively deletes folder and all its sub contents
* `rm -ri folder` - recursively deletes folder and all its sub contents but `with a prompt`

## Killing a Program 
> Do the following below if getting stucked in a program and conventional ways like `ctrl c, ctrl d or q doesnt work`
1. Use arrow command at top right to go to 2nd terminal
2. Perform `htop` to check Process identifier of the `process` that has hanged or unable to quit
3. Scroll to the particular process and press `fn + f9` key and select 9 `SIGKILL`
4. Head back to first terminal and process should be killed
