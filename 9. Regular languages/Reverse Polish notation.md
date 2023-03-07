| Term                              | Description                                                 | Comment                                                                                                                                                                                   |
| --------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Infix                             | The operator comes between the operands. <pre>a*(b+c)</pre> | This is the notation used in mathematics                                                                                                                                                  |
| Prefix (Polish Notation)          | The operator comes before the operands <pre>/*a+bcd</pre>   | This was invented in 1924                                                                                                                                                                 |
| PostFix (Reverse Polish Notation) | The operator comes after the operands <pre>abc+*d/</pre>    | During the 1950s Reverse Polish was devised as a way to do mathematics without braces. The system is used extensively in computer algorithms because evaluation can be done using a stack |

## RPN - Why Use It?

Eliminates the need for brackets in sub-expressions as the order of evaluation is unambiguous. The algorithm for evaluation postfix expressions is simpler than for infix expressions.

### How to Convert Expressions

#### Translation by Numbering

- Start on the left with the number 1
- If the token is an operand, allocate the next number
- Ignore brackets except in so far as they affect the order of calculation
- If it is an operator, and enough operands are available, then back up and number the operator, otherwise advance to next token
- Keep order of precedence in mind, as it might require some reading ahead
- When finished write down the tokens in numerical order

```
a * ( b + c ) / d

1     2   3

1     2 4 3

1 5   2 4 3

1 5   2 4 3     6

1 5   2 4 3   7 6

a b c + * d /
```

#### Translation by Bracketing

- Add brackets to make explicit the order of precedence, including exponentiation
- Move the operator in each set of brackets to the end position
- Remove all the brackets

```
a * ( b + c ) / d

( ( a * ( b + c ) ) / d )

( ( a * ( b c + ) ) / d )

( ( a ( b c + ) * ) / d )

( ( a ( b c + ) * ) d / )

a b c + * d /

a b c + * d /
```
