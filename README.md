# Scheme
Implementation of a Scheme interpreter with full Read-Eval-Print-Load functionality

## Description
This interpreter is for a subset of the Scheme language. The subset of the language used in this project is described in the functional programming section of [Composing Programs](http://composingprograms.com/pages/32-functional-programming.html). 
Since we only include a subset of the language, this interpreter will not exactly match the behavior of other interpreters.

## Scheme features
### Read-Eval-Print. 
The interpreter reads Scheme expressions, evaluates them, and displays the results.
```
scm> 2
2
scm> (+ 2 3)
5
scm> ((lambda (x) (* x x)) 5)
25
```
### Load. 

You can load a file by passing in a symbol for the file name. For example, to load tests.scm, evaluate the following call expression.
```
scm> (load 'tests)
```
### Symbols.
Various dialects of Scheme are more or less permissive about identifiers (which serve as symbols and variable names).

Our rule is that:

An identifier is a sequence of letters (a-z and A-Z), digits, and characters in !$%&*/:<=>?@^_~-+. that do not form a valid integer or floating-point numeral and are not existing special form shorthands.

Our version of Scheme is case-insensitive: two identifiers are considered identical if they match except possibly in the capitalization of letters. They are internally represented and printed in lower case:
```
scm> 'Hello
hello
```

Source: https://inst.eecs.berkeley.edu/~cs61a/sp21/proj/scheme/
