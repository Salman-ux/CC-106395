# CC Spring 2021: Project Phase 1 #
## PROJECT MEMBERS ##
StdID | Name
------------ | -------------
*62636* | *Salman AHmad* 
60852 | Muhammad Shuja

## Language Selected ##

Mini pascal

#
<program> ::=	program <identifier> ; <block> .
<block> ::=	<variable declaration part>
<procedure declaration part>
<statement part>
<variable declaration part> ::=	<empty> |
var <variable declaration> ;
    { <variable declaration> ; }
<variable declaration> ::=	<identifier > { , <identifier> } : <type>
<type> ::=	<simple type> | <array type>
<array type> ::=	array [ <index range> ] of <simple type>
<index range> ::=	<integer constant> .. <integer constant>
<simple type> ::=	<type identifier>
<type identifier> ::=	<identifier>
<procedure declaration part> ::=	{ <procedure declaration> ; }
<procedure declaration> ::=	procedure <identifier> ; <block>
<statement part> ::=	<compound statement>
<compound statement> ::=	begin <statement>{ ; <statement> } end
<statement> ::=	<simple statement> | <structured statement>
<simple statement> ::=	<assignment statement> | <procedure statement> |
<read statement> | <write statement>
<assignment statement> ::=	<variable> := <expression>
<procedure statement> ::=	<procedure identifier>
<procedure identifier> ::=	<identifier>
<read statement> ::=	read ( <input variable> { , <input variable> } )
<input variable> ::=	<variable>
<write statement> ::=	write ( <output value> { , <output value> } )
<output value> ::=	<expression>
<structured statement> ::=	<compound statement> | <if statement> |
<while statement>
<if statement> ::=	if <expression> then <statement> |
if <expression> then <statement> else <statement>
<while statement> ::=	while <expression> do <statement>
<expression> ::=	<simple expression> |
<simple expression> <relational operator> <simple expression>
<simple expression> ::=	<sign> <term> { <adding operator> <term> }
<term> ::=	<factor> { <multiplying operator> <factor> }
<factor> ::=	<variable> | <constant> | ( <expression> ) | not <factor>
<relational operator> ::=	= | <> | < | <= | >= | >
<sign> ::=	+ | - | <empty>
<adding operator> ::=	+ | - | or
<multiplying operator> ::=	* | div | and
<variable> ::=	<entire variable> | <indexed variable>
<indexed variable> ::=	<array variable> [ <expression> ]
<array variable> ::=	<entire variable>
<entire variable> ::=	<variable identifier>
<variable identifier> ::=	<identifier>


## Lexical Grammar Of Mini Pascal ##


<constant> ::=	<integer constant> | <character constant> | <constant identifier>
<constant identifier> ::=	<identifier>
<identifier> ::=	<letter> { <letter or digit> }
<integer constant> ::=	<digit> { <digit> }
<character constant> ::=	'< any character other than '     >'  |  ''''
<letter> ::=	a | b | c | d | e | f | g | h | i | j | k | l | m | n | o | 
p | q | r | s | t | u | v | w | x | y | z | A | B | C |
D | E | F | G | H | I | J | K | L | M | N | O | P
| Q | R | S | T | U | V | W | X | Y | Z
<digit> ::=	0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9
<special symbol> ::=	+ | - | * | = | <> | < | > | <= | >= |
( | ) | [ | ] | := | . | , | ; | : | .. | div | or |
and | not | if | then | else | of | while | do |
begin | end | read | write | var | array |
procedure | program
<predefined identifier> ::=	integer | Boolean | true | false

## Language CFG ##
<program> ::= "program" <id> ";" <block> "." 
<declaration> ::= "var" <id> { , <id> } ":" <type> | 
"procedure" <id> "(" parameters ")" ";" <block> | 
"function" <id> "(" parameters ")" ":" <type> ";" <block> 
<parameters> ::= [ "var" ] <id> ":" <type> { "," [ "var" ] <id> ":" <type> } | <empty> 
<type> ::= <simple type> | <array type> 
<array type> ::= "array" "[" [<integer expr>] "]" "of" <simple type>
<simple type> ::= <type id> 
<block> ::= "begin" <statement> { ";" <statement> } [ ";" ] "end" 
<statement> ::= <simple statement> | <structured statement> | <declaration>
<empty> ::=
<simple statement> ::= <assignment statement> | <call> | <return statement> | 
< read statement> | <write statement> | <assert statement> 
<assignment statement> ::= <variable> ":=" <expr> 
<call> ::= <id> "(" <arguments> ")" 
<arguments> ::= expr { "," expr } | <empty> 
<return statement> ::= "return" [ expr ] 
<read statement> ::= "read" "(" <variable> { "," <variable> } ")" 
<write statement> ::= "writeln" "(" <arguments> ")" 
<assert statement> ::= "assert" "(" <Boolean expr> ")" 
<structured statement> ::= <block> | <if statement> | <while statement> 
<if statement> ::= "if" <Boolean expr> "then" <statement> | 
"if" <Boolean expr> "then" <statement> "else" <statement> 
<while statement> ::= "while" <Boolean expr> "do" <statement>
<expr> ::= <simple expr> | 
<simple expr> <relational operator> <simple expr> 
<simple expr> ::= [ <sign> ] <term> { <adding operator> <term> } 
<term> ::= <factor> { <multiplying operator> <factor> } 
<factor> ::= <call> | <variable> | <literal> | "(" <expr> ")" | "not" <factor> | < factor> "." "size" 
<variable> ::= <variable id> [ "[" <integer expr> "]" ] 
<relational operator> ::= "=" | "<>" | "<" | "<=" | ">=" | ">" 
<sign> ::= "+" | "-" 
<adding operator> ::= "+" | "-" | "or" 
<multiplying operator> ::= "*" | "/" | "%" | "and" 
