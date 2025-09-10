Purpose

This program is a Lexical Analyzer that classifies different tokens of a C-like language. It can identify:
Operators (arithmetic, relational, logical, bitwise, assignment)
Keywords
Identifiers
Constants (float, integer)
Comments

How It Works

1. Definitions Section
Here patterns (regular expressions) are defined using names, which makes rules easier to read.
keyword → matches reserved words like int, char, if, else, while, etc.
letter → matches any alphabet a–z or A–Z.
digit → matches any digit 0–9.
float → matches decimal numbers such as 12.34 or 45..
integer → matches whole numbers made only of digits.
arth → matches arithmetic operators like + - * /.
rel → matches relational operators like <, <=, ==, !=, etc.
log → matches logical operators like &&, ||, !.
bit → matches bitwise operators like &, <<, >>, ^.
assign → matches the assignment operator =.
comment → matches single-line comments starting with //.

2. Rules Section
Each rule checks if the input matches a defined pattern, then executes an action:
If input is an arithmetic operator, print:
+ is an arithmetic operator If input is a relational operator, print:
>= is a relational operator If input is a logical operator, print:
&& is a logical operator
If input is a bitwise operator, print:
>> is a bitwise operator
If input is an assignment operator, print:
= is an assignment operator
If input matches a keyword, print:
int is a keyword
If input starts with a letter and continues with letters or digits, it is a valid identifier:
myVar1 is a valid identifier
If input matches a float constant, print:
12.45 is a float constant
If input matches an integer constant, print:
100 is an integer constant

If input matches a comment, print:
"//hello" is a commen

3. Main Function
Calls yylex() which starts the lexical analysis.
The program keeps scanning the input until all tokens are classified.

Examples of Input and Output

Input: int → Output: int is a keyword
Input: a1b2 → Output: a1b2 is a valid identifier
Input: 123 → Output: 123 is an integer constant
Input: 45.67 → Output: 45.67 is a float constant
Input: = → Output: = is an assignment operator
Input: >= → Output: >= is a relational operator
Input: && → Output: && is a logical operator
Input: //test → Output: "//test" is a comment

Summary
This Lex program works as a mini lexical analyzer for C programs. It can successfully identify:
Tokens: keywords, identifiers, constants, comments.
Operators: arithmetic, relational, logical, bitwise, and assignment.
