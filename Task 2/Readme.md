# RISC-V Optimization and Disassembly Analysis

This repository contains the results of Task 2: investigating the effects of compiler optimization flags `-O1` and `-Ofast` on a RISC-V binary compiled using the `riscv64-unknown-elf-gcc` toolchain and analyzed using `objdump`.

## 📄 Task Objective

- Write a simple C program.
- Compile it using `-O1` and `-Ofast` flags.
- Disassemble the resulting RISC-V binaries.
- Compare the assembly output from each optimization level.
- Upload screenshots and dump files to GitHub for reference.

## 🛠️ Tools Used

- `riscv64-unknown-elf-gcc` — for cross-compilation
- `riscv64-unknown-elf-objdump` — for disassembly
- `Spike` — for RISC-V simulation (referenced via tutorial)
- `grep`, `less`, `cat` — for analyzing output
- Ubuntu VirtualBox environment

## 🧑‍💻 Source Code

```c
// sum.c
#include <stdio.h>
int main() {
    int a = 5, b = 3;
    int sum = a + b;
    printf("Sum is %d\n", sum);
    return 0;
}
 # COMPILATION COMMANDS
riscv64-unknown-elf-gcc -O1 -o sum_O1 sum.c
riscv64-unknown-elf-gcc -Ofast -o sum_Ofast sum.c
## DISASSEMBLY COMMANDS
riscv64-unknown-elf-objdump -D sum_O1 > sum_O1.dump
riscv64-unknown-elf-objdump -D sum_Ofast > sum_Ofast.dump
