## Moving Files
* `mkdir d1` - create directory d1
* `touch f1` - create file f1
* `mv f1 d1` - move f1 into d1
* `mkdir bigdir` - make another directory bigdr
* `mv d1 bigdir` - move D1 into bigdr
* `mv . ../..` - wont work because `cannot move current directory of .`

## Renaming directories
> No rename feature in linux so use `mv command to`. Criteria is that the new name has to not exist
* `mv bigdir smalldir` - changes bigdir to smalldir `since smalldir` does not exist
* `mv otherdir/f1 smalldir/f2` - moves f1 into small dir and renames it f2

#### Overwriting existing file
* Assuming we have 2 files `f5 and f6`
* `mv f6 f5` would result in f5 contents being lost and f6 contents moved into f5 and f6 is deleted
* It essentially means renaming f6 to f5
* `mv -i f6 f5` prompts before u move f6 contents and rename it to f5


## Copying
#### Copying files
* `cp f1 f2` - copies the contents of f1 into f2
* `cat f2 > f3` - this works in terms of copying the content of f2 into f3 too

#### Copying Directories
* `cp -r d1 d2` - copies the contents of d1 into another new directory d2 
* `cp -r d1 d2` - if u run this again with d2 already existing, it copies the contents of d1 as a subfolder into d2
* `cp -ri d1 d2` - if ran for the 3rd time it overwrites, so now we include `i` as a prompt to check if we want to overwrite


