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
* `pwd` - print working directory of where u are in
* `ls` - lists the files & directories inside working directory
* `ls -a` - shows all files and hidden files in pwd 
* `cd / ` - change directory to root directory
* `cd ` - cd alone would always bring us to the home user folder
* `cd ./sys` - from curr directory change to sys 
* `cd ../..` - brings us to root directory if we are in `~` (relative path)
* `cd /sys` - absolute path because starts with `/` aka the root