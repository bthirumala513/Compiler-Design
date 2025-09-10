%{
#include <stdio.h>
%}

keyword (int|char|float|if|else|while|for|return|switch|case|default|break|continue|struct|union|enum|typedef|static|extern|const|volatile|sizeof|void|do|signed|unsigned|goto|register|aut|long|short|inline)
letter [a-zA-Z]
digit [0-9]
float ([0-9]*\.[0-9]+|[0-9]+\.)
integer {digit}+

arth    [\+|\-|\*|\/]
rel     (<|>|<=|>=|!=|==)
log     (\|\||&&|!)
bit     (&|<<|>>|\^)
assign  (=)
comment (\/\/.*)

%%
{arth}		{printf("%s is an arthimetic operator",yytext);}
{rel}		{printf("%s is a relational operator",yytext);}
{log}		{printf("%s is a logical operator",yytext);}
{bit}		{printf("%s is a bitwise operator",yytext);}
{assign}        {printf("%s is an assignment operator",yytext);}
{keyword}	{printf("%s is a keyword",yytext);}
{letter}({letter}|{digit})* {printf("%s is a valid identifier",yytext);}
{float} {printf("%s is a float constant",yytext);}
{integer} {printf("%s is an integer constant",yytext);}
{comment}	{printf("\"%s\" is a comment",yytext);}
%%

void main()
{
yylex();
}
