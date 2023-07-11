# Compiler
This repository contains a compiler implemented in C for a specific programming language. The compiler follows the language specifications provided in "Language Specifications.pdf".

### Project Overview
The compiler is responsible for parsing input files according to the language specifications. If the input is both syntactically and semantically correct, the compiler can generate corresponding assembly-level code. Test cases have been provided in the "testcases" directory for evaluating the compiler's functionality.

### Compatibility
The code is compatible with GCC version 5.4.0 and has been tested on Ubuntu 16.04. To run it on Windows, you will need to use [Cygwin](https://www.cygwin.com/).

### How to Use
To create the compiler:

1.Navigate to the "Compiler" directory.
2.Run the command: make.
3.This will create an executable file named "compiler".

## To test the compiler on a test case:

1.Ensure that you are in the directory containing the "compiler" executable.
2.Run the command: `./compiler <RELATIVE_PATH_TO_TESTCASE_FILE> <NAME_OF_ASM_FILE>`.
3.Choose one of the available options (0-10) to test the desired feature.
4.To generate assembly-level code, select option 10.
5.Choose option 0 to exit (Ctrl + C will result in no output in the ASM file).
6.To run the generated ASM file, use the following commands: `nasm -felf64 code.asm && gcc code.o && ./a.out` (Replace "code.asm" with the actual name of the ASM file).



### To create the compiler 
1.  `cd Compiler`
2.  `make`
3.  This will create an executable file named _compiler_

### To test the compiler on a testcase
1.  Ensure you are in the directory containing the _compiler_ executable
2.  Run `./compiler <RELATIVE_PATH_TO_TESTCASE_FILE> <NAME_OF_ASM_FILE>`
3.  Choose among the 11 options to test the feature you want.
4.  To create assembly-level code , choose option 10.
5.  Choose option 0 to exit. (Ctrl + C would result with no output in the ASM file)
6.  To run the asm file `nasm -felf64 code.asm && gcc code.o && ./a.out` (Using code.asm as the name of the asm file in this example)

### Stages of Compiling a Test Case (Option 10)
                                              
 |    Stage    |     Details  |
| :------------- | :----------: |
|  Lexical Analysis | Categorizes the contents of the input file into tokens based on the language specifications.|
| Syntax Analysis   | Creates a Parse Tree based on the tokens returned by the lexer. If any errors occur, compilation stops.|
| Semantic Analysis |Creates an Abstract Syntax Tree (AST) from the corresponding Parse Tree and populates the Symbol Table.|
| Code generation | Generates assembly-level code. Code generation is limited to test cases that have a single main function and handle only integers.|


## Contributors
The team members of this project were:
* [Karan Bagle](https://github.com/karanbagle)
* [Girish Bisane](https://github.com/girishb007)
* Siddharth Mohite
