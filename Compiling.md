## Interpreter vs Compiler

#### Interpreter
* Reads your instructions one-by-one and `immediately` translates it to the machine for the machine to execute
* Pros: Anytime the machine executes your instruction incorrectly, you can `spot the error` immediately and change instructions accordingly
* Cons: Slow process as machine has to wait for each of your instructions each time `before executing`.

#### Compiler 
* Compiler translates your whole list of instructions into a `binary file` and gives it back to you
* Whenever you have the `binary file`, you can then execute it as and when u want to
* Pros: Very fast process
* Cons: Unable to spot errors as easily


## Compiling a C program on Linux
* `gcc program.c -o program` which outputs the binary as `program`
* `./program` - to execute the binary
* `gcc -std=c11 -Wall -fmax-errors=10 -Wextra program.c -o program`
    1. use 2011 c standard for compiler
    2. `Wall` print out all warnings
    3. `-fmax-errors=10` output max. 10 errors 
    4. `-Wextra` output extra warnings too