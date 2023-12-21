# Syntax-Parser
lexical analyzer that we developed in Project 1 and develop a recursive descent syntax parser that can validate the syntax in the input files provided by the user.


The source code file provided by the user will be written in a new programming language called “DCooke” and is
based upon the following grammar (in BNF):



P ::= S



S ::= V=E | read(V) | write(V) | do { S } while (C) | S;S



C ::= E < E | E > E | E == E | E != E | E <= E | E >= E



E ::= T | E + T | E - T



T ::= F | T * F | T / F



F ::= (E) | O | N | V



O ::= V++ | V--



V ::= a | b | … | y | z | aV | bV | … | yV | zV



N ::= 0 | 1 | … | 8 | 9 | 0N | 1N | … | 8N | 9N


Your parser should read the given DCooke source code file then, using your lexical analyzer, identify
lexemes/tokens one at a time to ensure they can be aligned with known BNF rules for the language. For this
language, P::=S would be the root of the parse tree. Your parser may print out the steps it takes during
execution if you wish (similar to the provided parser) but that is not required. The following is the only required
output and exit codes from your parser:



1) Your solution must print out “DCooke Parser :: R<#>” as the first line of output with <#> being replaced
by your R#. The double colon “::” is required for correct grading of your submission.



2) If the provided user file is free of syntax errors:
a. Your solution must print out “Syntax Validated” as the last line of output.
b. Your solution must return with an exit code of 0.



3) If the provided user file contains syntax errors:
a. Your solution must print out “Error encounter: The next lexeme was <lexeme> and the next
token was <token>”
i. Where <lexeme> is the lexeme that caused the problem (examples: “x”, “<>”)
ii. Where <token> is the uppercase name of the token (examples: “IDENT”, “UNKNOWN”)
b. Your solution must return with an exit code of 1.



4) If the user did not provide a file as input:
a. Your solution must display an appropriate error message.
b. Your solution must return with an exit code of 2.



5) If the user did provide a file as input but the file does not exist:
a. Your solution must display an appropriate error message.
b. Your solution must return with an exit code of 3.
