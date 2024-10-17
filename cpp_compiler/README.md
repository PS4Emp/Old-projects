# Mini C++ Compiler showing if-else, for loop

This was made back in 18-19. Some changes were made in 2021 as well. 



Problem Statement
The objective of this project is to design and implement a compiler for a simple programming language similar to C++, utilizing the Lex and Yacc compiler generation tools, along with a basic GUI in C++.

This Mini Compiler project, developed for the Compiler Design course, focuses on generating intermediate code for specific language constructs, including conditional statements, loops, and the ternary operator. The primary goal is to produce optimized intermediate code from the provided C++ source code, achieved through the following steps:

Generate a symbol table after evaluating expressions
Create an Abstract Syntax Tree (AST) for the code
Produce three-address code and corresponding quadruples
Implement code optimization
The main tools employed in this project are LEX, which identifies predefined patterns and generates tokens for matches, and YACC, which parses input for semantic meaning, generating an abstract syntax tree and intermediate code. Additionally, Python is used for optimizing the intermediate code produced by the parser.

Design Strategy
Symbol Table Creation
The symbol table manages error detection and expression evaluation. It addresses issues such as undeclared variables, redeclaration of variables, and syntax errors like missing semicolons.

Intermediate Code Generation
The intermediate code generator receives an annotated syntax tree from the semantic analyzer, converting it into a linear representation. This intermediate code is designed to be machine-independent.

Code Optimization
The code optimizer maintains a key-value mapping akin to the symbol table structure to track variables and their values (possibly after expression evaluation). This structure is utilized for constant propagation, constant folding in sequential blocks, and dead code elimination.

Error Handling
To facilitate syntax validation, an abstract syntax tree (AST) is employed. ASTs are essential data structures in compilers that represent program code structure. Typically, an AST results from the syntax analysis phase and serves as an intermediate representation throughout various compiler stages, significantly influencing the final output.

In this project, the AST represents the syntactic flow of the code. The grammar symbols are managed using %left and %right fields. The AST allows us to separate parsing and validation logic from implementation. During the syntax validation phase, if parsing issues arise, the AST parser can be examined, while discrepancies in code results can be investigated through the code interpreting the AST.



