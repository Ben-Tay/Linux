## Memory Management
> Operating system stores our data through `memory management`
## Random Access Memory (RAM)
> Temporary memory that is easy & quick to access for purposes such as `executing programs` or to store values for variables

> Also known as `volatile memory`

> For simplicity, can see RAM as a sequence of binary memory cells, each populated with a 0 or a 1.
* We call each cell `1-bit`
* A group of bits clustered together is what forms a `word`.
* A word is the `fundamental unit of data` that
can be moved between the RAM and the computer processor.
* The size of a word is thus expressed in number of bits -- that is, number of memory cells -- or in bytes
* 1 byte = 8 bits
* Modern personal computers and modern processors more ordinarily tend to use `8, 16, 32, or even 64` bits to form one word, though other word sizes are possible. 

> GROUPING memory cells into `words` allows for memory addressing. A memory address is the `address` for the location of a word in memory

> This technique of memory addressing allows for optimization of memory usage at a very precise level, or of performance in terms of execution speed, `as we could traverse the computer's memory word for word`. This is an extremely powerful tool for application developers.

## Non-volatile Memory (Storage)
> Typically data stored on a hard-disk drive and is `more long-lasting` and permanent

## Managing Memory with the CLI
* `free -b/k/m/g` - check the amount of free memory in bytes, kilobytes, megabytes, or gigabytes
* `top` - also shows memory used
* `htop` - does the same as top with better GUI, use `fn + f6 key` to sort by `M_Size` to see memory

##### C program for user input
```sh
# printf buffer depends on linux system used
/*Write your C code here*/
#include <stdio.h>

int main() {
# need to add a new line after printf as its buffered
	char firstName[50];
	char familyName[50];
	int age;
	printf("What is your family name?\n");
	scanf("%s", familyName);
	printf("What is your first name?\n");
	scanf("%s", firstName);
	printf("What is your age?\n");
	scanf("%d", &age);
	printf("%s %s %d\n", familyName, firstName, age);
	return 0;
}

# Alternatively without new line, use flush
/*Write your C code here*/
#include <stdio.h>

int main() {
	char firstName[50];
	char familyName[50];
	int age;
	printf("What is your family name?");
	fflush(stdout);
	scanf("%s", familyName);
	printf("What is your first name?");
	fflush(stdout);
	scanf("%s", firstName);
	printf("What is your age?");
	fflush(stdout);
	scanf("%d", &age);
	printf("%s %s %d\n", familyName, firstName, age);
	return 0;
}
```
> `Virtual Memory (VIRT)` is  NOT THE SAME as physical memory. VIRT is the amount of memory being reserved whereas physical memory is the amount of memory being `used`.

#### Use scanf and file redirection to simulate an input

Given we have an `answers` text file with the following content:
```
sharrock
remi
18
```

1st way: Cat output of answers into ur input program
* `cat answers | ./program`

2nd way: redirect the input of answers into ur input program
* `./program < answers`


## Use other ways instead of scanf for userinput
> Scanf can be dangerous at times as split user input to 1 question may be used to answer other questions
* `sharrock remi 18` in one input line is only supposed to answer the first question but answers all 3

* can use `fgets or getline` instead where getline is only compatible with POSIX systems