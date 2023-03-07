Regular expressions are patterns used to specify a set of strings. They are expressed using a special notation.

RegEx is used for finding particular words in a stream, combinations of characters in strings and defining a set of acceptable strings in a language.

| Symbol | Meaning                                                        |
| ------ | -------------------------------------------------------------- |
|        | Members side by side must appear in that sequence              |
| \|     | Separates alternatives                                         |
| \*     | Indicates that there are zero or more of the preceding element |
| \+     | Indicates that there is one or more of the preceding element   |
| \?     | Indicates that there are zero or one of the preceding element  |
| ()     | Used to identify groupings                                                               |

ie A+B {AB, AAB, ABB etc}

## Regular Language

A language is regular if it can be represented by a regular expression or a finite state machine.

(You can also define a regular expression as a finite state machine but it's so easy and much effort)
