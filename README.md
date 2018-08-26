# Simple Risc-V Assembler

Assembler for `rv32i` written in C++.
Converts a `std::string` into a `std::vector` containing the binary-instructions.
Currently no error-detection is implemented, hence any error will be ignored!

supported:
- rv32i
- flags
- word-data declaration

not supported:
- cssr*-instructions
- fence-instruction
- linking
- sections
- all data declarations (.space, etc.)
- alias-instructions (j, ret, etc.)
