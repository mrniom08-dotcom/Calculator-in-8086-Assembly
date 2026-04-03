# Calculator-in-8086-Assembly
This project implements a simple arithmetic calculator using 8086 Assembly language for DOS. The calculator takes two single-digit operands and an operator as input, performs the corresponding arithmetic operation, and displays the result. It handles addition, subtraction, multiplication, division, and includes basic error handling for invalid operators and division by zero.

#Features:

Accepts two single-digit operands (0-9)
Supports the following operators:
+ (Addition)
- (Subtraction)
* (Multiplication)
/ (Division)
Displays the result in decimal format
Handles division by zero with a custom message (Infinity)
Handles invalid operators with a custom message
Handles negative results
Result formatting includes CR, LF, and ends with $ for DOS string compatibility

##How it works:

Reads user input via DOS interrupt (int 21h):

First operand (a digit 0–9)
Arithmetic operator (+, -, *, /)
Second operand (a digit 0–9)
Converts ASCII characters to numeric values by subtracting '0'.

Performs the specified arithmetic operation:

Addition
Subtraction
Multiplication
Division (with division-by-zero check)
Handles special cases:

Invalid operator: Displays "Invalid operator" message.
Division by zero: Triggers a custom interrupt handler to print "Infinity".
Formats and displays the result:

Adds an equal sign (=) before the result.
Handles negative results by printing a minus sign and converting the result to positive.
Converts the numeric result into ASCII characters (supports two-digit results).
Uses int 21h function 09h to print the formatted result.
