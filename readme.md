# CC Spring 2021: Project Phase 1 #
## PROJECT MEMBERS ##
StdID | Name
------------ | -------------
*62636* | *Salman AHmad* 
60852 | Muhammad Shuja

## Language Selected ##

Mini C 

## Example of main constructs ##

int main(){

} 

## Example of for loop constructs ##

for(int i=0;i<3;i++)
{
   printf("Welcome to CC Project");
}

## Example of if condition constructs ##
  int a = 5;
   int b = 20;
   int c ;

   if ( a && b ) {
      printf("Line 1 - Condition is true\n" );
   }
	
   if ( a || b ) {
      printf("Line 2 - Condition is true\n" );
   }
   
   /* lets change the value of  a and b */
   a = 0;
   b = 10;
	
   if ( a && b ) {
      printf("Line 3 - Condition is true\n" );
   } else {
      printf("Line 3 - Condition is not true\n" );
   }
	
   if ( !(a && b) ) {
      printf("Line 4 - Condition is true\n" );
   }
	
}

## Example of while loop constructs ##

i=1;
while(i<=10)
{
  printf("%d ",i);
  i++;
} 

## Example of array constructs ##

float marks[3] = {97.5, 50.3, 80.7};



## Lexical Specification ##


1.program →declaration-list
2.declaration-list → declaration-list declaration | declaration
3.declaration → var-declaration | fun-declaration
4.var-declaration → type-specifier ID; 
5.type-specifier → int| void| float
6.fun-declaration → type-specifier ID( params ) compound-stmt
7.params → param-list |void| λ
8.param-list → param-list, param | param
9.param → type-specifier ID
10.compound-stmt → {local-declarations statement-list}
11.local-declarations →local-declarations var-declaration | λ
12.statement-list → statement-list statement | λ
13.statement → expression-stmt | compound-stmt | selection-stmt | iteration-stmt | jump-stmt
14.expression-stmt → expression ;| ;
15.selection-stmt → if(expression )statement 
      |if ( expression)statement elsestatement
16.iteration-stmt →while-statement | for-statement
17.while-statement→ while ( expression )statement
18.for-statement →for(expression;expression;expression)statement
19.jump-stmt → return;| return expression;| break ;
20.expression → id-assign=expression | simple-expression
21.id-assign→ID
22.simple-expression   → additive-expression relop additive-expression | additive-expression
23.relop →<= | < | > | >= | == | !=|&&| ||
24.additive-expression  → additive-expression addop term | term
25.addop → + | -
26.term → term mulop factor | factor
27.mulop → *| /
28.factor →(expression ) | id-assign| call | num
29.call → ID(args )
30.args → arg-list | λ
31.arg-list → arg-list , expression | expression
32.num →pos-num|neg-num
33.pos-num→+value | value
34.neg-num→-value
35.value →INT_NUM|FLOAT_NUM


## Language CFG ##
PROG -> LIB FUNCTION | ;
