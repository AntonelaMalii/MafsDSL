## Table of contents
* [Goal of the Project](#goaloftheproj)
* [Grammar](#grammar)
* [Semantic Rules](#semanticrules)
* [Technologies](#technologies)
## Goal of the Project
The goal of the project is to design a DSL that is capable of computing and displaying in graphic format calculus functions, equations and systems of equations. Development of this project include some objectives mentioned below:
* Defining the grammar of the DSL.
* Defining semantic and syntactic rules.
* Implement our own lexer and parser.
* Creating the DSL according to the requirements. 
* Test the DSL Project.

## Grammar 
Grammar of a programming language is a technical way of describing a set of formal rules that overviews how the programming language is constructed and presents the valid tokens and lexemes. 

The code of any programming language can be implemented without any errors and troubles according to a specified valid grammar that should respect a set of predefined rules of definition of the grammar in general.

The grammar for the domain specific language consists of a 4-tuple G = {T, N, P, S} where :

* “T”-set of terminals.
* “N”-set of non-terminal.
* “S”- start symbol.
* “P” – the set of production rules for generating valid sentences of the language.

The set of Production Rules of MafsDSL are specified in the grammar.txt file.

## Semantic Rules
Semantic rules add additional constraints on the valid program besides the constraints implied by the grammar.

Semantic constraints of our domain specific language can be formulated as it follow:

* The declaration of variables should contain the token “VAR” followed by an identifier the sign = and an expression 
* An expression can be an arithmetical expression or a comparison expression.
* When it comes to comparison expression we obtain a false or true value depending on a set of operators <,>,<=,>=,=.
* We can concatenate 2 comparison expression in one with the tokens AND, OR, NOT and also obtain a false or true value in the result.
* Arithmetical expression are first divided in terms by the presence of plus/minus sign. 
* If the term contains mul/div sign, it is divided to a new construction of factors and *,/ signs, else the term is considered to be just a simple factor.
* The presence of parentheses is also changing the behavior of the way how the operations are realised.
* A factor can derive into a variable/identifier, or a number formed by some digits.
* A function can be declared with the usage of the token FUN followed by an identifier/name of the function and some paratheses with the variables that are used in the function,delimited by a comma. We can have as many variables as we want.
* After the declaration of the variables that are used we put the arrow sign which points to the expression that represents the function.
* To find the value of the function we can simply then use the name of the function followed by specific values for variables in parentheses.
* The IF control structure is focused on working with expressions. We use the tokens THEN and ELSE to specify 2 more expressions that will be realised based on the boolean result of the expr that is given along with the IF token.




## Technologies
Project is created with:

```
$ Python version 3.8
