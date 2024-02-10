# Custom Shell for xv6 and UNIX
###Noreen Sulehry

## Overview
This custom shell is designed to enhance the command line interface experience in xv6 and compatible UNIX environments. Featuring support for the sequence execution operator `;`, and the capability to understand and execute commands enclosed within parentheses `()`, this shell aims to provide a more flexible and powerful command execution mechanism. It supports up to 2 levels of nesting with parentheses, thereby enabling more complex command execution flows.

## Features
- **Sequence Execution (`;`)**: Execute multiple commands in sequence, allowing for a series of operations to be performed one after the other.
- **Command Grouping (`()`)**: Group commands within parentheses to control the order of execution, supporting up to 2 levels of nesting for complex command chains.
- **Environment Compatibility**: Fully compatible with xv6 and UNIX environments, ensuring that commands such as `echo`, `cat`, and `wc` can be executed seamlessly.
- **Illegal Command Line Handling**: The shell is equipped to identify and reject illegal command lines, providing error messages to help correct command syntax.

## Getting Started

### Prerequisites
- A working xv6 or UNIX environment.
- GCC for compiling the shell program.

### Installation
1. Clone the xv6-riscv repository from github https://github.com/mit-pdos/xv6-riscv/blob/riscv/user/sh.c
2. Navigate to the project directory.
3. Compile the shell using the command:
   make
   make clean
   make qemu-nox

- You will be greeted with the S2024$ prompt, indicating that the shell is ready to accept commands.

### Contributing
- Contributions to improve the shell, add new features, or fix bugs are warmly welcomed. Please feel free to submit pull requests or create issues for discussion on enhancements or issues encountered.

### Acknowledgments
- Gratitude to the xv6 development community for their educational resources.
- This `README.md` file is structured to provide a clear introduction, detailed setup instructions, usage examples, and contribution guidelines, making it accessible to users and potential contributors. Adjust the paths, commands, and examples as necessary to match your project specifics.
