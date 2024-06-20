
** Lox Grammar (ambiguous)
#+BEGIN_EXAMPLE
expression     → literal
               | unary
               | binary
               | grouping ;

literal        → NUMBER | STRING | "true" | "false" | "nil" ;
grouping       → "(" expression ")" ;
unary          → ( "-" | "!" ) expression ;
binary         → expression operator expression ;
operator       → "==" | "!=" | "<" | "<=" | ">" | ">="
               | "+"  | "-"  | "*" | "/" ;
#+END_EXAMPLE

The above grammar is ambiguous. For example, ~6 / 3 - 1~ can have two parse trees:
#+BEGIN_EXAMPLE
  /                OR             -
 / \                             / \
6   -                           /   1
   / \                         /\
  3   1                       6  3
#+END_EXAMPLE

** Lox Grammar (unambiguous)
#+BEGIN_EXAMPLE
expression     → equality ;
equality       → comparison ( ( "!=" | "==" ) comparison )* ;
comparison     → term ( ( ">" | ">=" | "<" | "<=" ) term )* ;
term           → factor ( ( "-" | "+" ) factor )* ;
factor         → unary ( ( "/" | "*" ) unary )* ;
unary          → ( "!" | "-" ) unary
               | primary ;
primary        → NUMBER | STRING | "true" | "false" | "nil"
               | "(" expression ")" ;
#+END_EXAMPLE
