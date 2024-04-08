# Enhanced Memory Management System Calls for xv6
- Developed by GROUP# 16 (Noreen Sulehry - A20502963 and Fayez Ghosein - A20484297) 

## Overview
This project introduces two new system calls, `myV2p` and `myPages`, to the xv6 operating system. The `myV2p` system call translates a virtual address to its corresponding physical address, providing insights into the virtual-to-physical address mapping. The `myPages` system call lists the memory pages allocated to a specified process, including their physical addresses and properties, enhancing the observability of xv6's memory management.

## Features
- **Virtual to Physical Address Translation (`myV2p`)**: Converts a user-space virtual address to a physical address, identifying mappings and unmapped regions.
- **Process Memory Inspection (`myPages`)**: Displays detailed information about the memory pages allocated to a process, aiding in memory management analysis.
- **Error Handling**: Robust error handling for invalid inputs and special cases, ensuring system call reliability.
- **User-Space Testing Programs**: Included testing programs to demonstrate and validate the functionalities of the new system calls.

## Getting Started

### Prerequisites
- A working setup of xv6 on your machine.

### Installation and Execution
1. Clone the xv6 repository and ensure you have the latest version.
2. Apply the provided patch or merge the changes for the new system calls into your local xv6 source code.
3. Rebuild the xv6 kernel by running:
   make
   make clean
   make qemu-nox

4. Within the xv6 shell, you can now utilize the testing programs for `myV2p` and `myPages` to explore the new functionalities.

## Debugging with Valgrind
Valgrind is a powerful tool for detecting memory leaks and undefined behavior in programs. Although not directly applicable within xv6, the principles demonstrated can be applied to debugging similar issues in user programs developed for xv6.

### Usage Examples
- **Using `myV2p`**:
Run the provided `test_myV2p` user program to see examples of virtual to physical address translations.

- **Using `myPages`**:
Execute `test_myPages` with different process IDs to inspect their memory page allocations.

### Debugging Steps
#### Step 1: Compile Your Test Program with Debugging Symbols
To prepare your program for Valgrind analysis, compile it with debugging information. This allows Valgrind to provide detailed insights about where in your code the potential issues are detected. For instance, to compile a program named `test1.c`, you would use the following command: ```gcc -g test1.c -o test1```

Replace `test1.c` and `test1` with the names of your source file and the desired output file, respectively.

#### Step 2: Run Valgrind with Leak Checks Enabled
Next, execute your program under Valgrind's supervision to check for memory leaks. Use the `--leak-check=yes` option to enable detailed leak diagnostics: ```valgrind --leak-check=yes ./test1```

Again, replace `test1` with the name of your executable file.

#### Step 3: Analyze the Output
Valgrind will run your program and report any memory leaks or undefined behaviors it encounters. Review the output carefully; it will include information such as the number of bytes leaked, the location in your code where leaks occur, and suggestions for further actions to take.

### Contributing
Contributions to refine the system calls, extend their functionalities, or enhance the testing suite are highly encouraged. Feel free to fork the repository, make your changes, and submit a pull request.

### Acknowledgments
This project builds upon the foundational work of the xv6 operating system developed by MIT. Special thanks to the xv6 community for their invaluable resources and support.

---

This README provides a comprehensive guide to installing, using, and contributing to the enhanced memory management and debugging features in xv6. Tailor the instructions and examples to fit the specifics of your implementation and environment.
