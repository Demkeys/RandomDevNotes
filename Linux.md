----
Linux program execution process | What does a C program main function returns to

* What happens when you run a program? https://stackoverflow.com/questions/1204078/what-happens-when-you-run-a-program
* What happens when a computer program runs? https://stackoverflow.com/questions/5162580/what-happens-when-a-computer-program-runs
* Difference between exit() and return in main() function in C https://stackoverflow.com/questions/35471878/difference-between-exit-and-return-in-main-function-in-c
* Exit program x86 https://stackoverflow.com/questions/32415331/exit-program-x86
----
ANSI, C and Escape Sequences

* https://stackoverflow.com/questions/45612822/how-to-properly-add-hex-escapes-into-a-string-literal
* https://stackoverflow.com/questions/38482586/unknown-escape-sequence
* https://stackoverflow.com/questions/56284599/why-must-i-use-x1b-not-to-represent-an-escape-character
* https://stackoverflow.com/questions/3219393/stdlib-and-colored-output-in-c
* https://en.wikipedia.org/wiki/Escape_sequence
* https://en.wikipedia.org/wiki/Escape_sequences_in_C#Table_of_escape_sequences
* https://en.wikipedia.org/wiki/ANSI_C
* https://en.wikipedia.org/wiki/ANSI_escape_code
* https://en.wikipedia.org/wiki/Geometric_Shapes


Notes about escape sequences in C:
* \x is an escape sequence whereas 0x would be a hex literal.
* And escape sequence string can consist of chars or hex values. "\x1b[31m" can be written as "\x1b\x5b\x33\x32\x6d". In "\x1b[31m" 1b is hex for the ESC control code (since there is no way to enter ESC control code through the keyboard), whereas [31m are individual chars.
----
