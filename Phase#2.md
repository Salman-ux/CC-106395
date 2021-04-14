	
%{
#define ID 1
#define C 2
#define SYMBOL 3
#define PR 4
#define CC 5

%}

digit   [0-9]
letter [a-z]|[A-Z]
integerliteral  [0-9]
realliteral [0-9.0-9e-+0-9]


%%
[a-z]|[A-Z]|[0-9]|"_"*           printf("%d %s\n",ID,yytext);
"+"|"-"|"*"|"="|"<>"|"<"|">"|"<="|">="|"("|")"|"["|"]"|":="|"."|","|";"|":"|".."|"div"|"or"|"and"|"not"|"if"|"then"|"else"|"of"|"while"|"do"|"begin"|"end"|"read"|"write"|"var"|"array"|"procedure"|"program"	printf("%d %s\n",SYMBOL,yytext);
integer|Boolean|true|false	printf("%d %s\n",PR,yytext);

['a-zA-Z'|"a-zA-Z]*|[0-9]*|[[a-z]|[A-Z]|[0-9]]*	 printf("%d %s\n",C,yytext);


	

%%
  

int yywrap(){}

int main(){
  
yylex();
printf("\nNumber of Captial letters ");	
  
}


