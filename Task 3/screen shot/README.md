# 🧠 RISC-V Instruction Encoding Reference

This repository presents 15 unique RISC-V instructions, covering all six instruction formats: R, I, S, B, U, and J. Each entry includes:

- 🛠️ Assembly syntax  
- 🔢 32-bit binary encoding  
- 🧬 Instruction type  
- 📸 Screenshot (when available)

---

## 📘 R-Type Instructions

| Instruction         | Encoding   | Description                      |
|---------------------|------------|----------------------------------|
| `add a0, a1, a2`     | `00b50533` | a0 = a1 + a2                     |
| `sub a0, a1, a2`     | `40b50533` | a0 = a1 - a2                     |
| `and a3, a1, a2`     | `00c6f733` | a3 = a1 & a2                     |
| `xor a0, a1, a2`     | `00b54533` | a0 = a1 ^ a2                     |

---

## 📗 I-Type Instructions

| Instruction         | Encoding   | Description                      |
|---------------------|------------|----------------------------------|
| `addi a0, a1, 10`    | `00a50513` | a0 = a1 + 10                     |
| `lw a0, 0(a1)`       | `00052503` | Load word from [a1] into a0     |
| `jalr a0, a1, 0`     | `00050567` | Jump to address in a1           |
| `sext.w a0, a1`      | `0005151b` | Sign-extend 32-bit value in a1  |

---

## 📙 S-Type Instructions

| Instruction         | Encoding   | Description                      |
|---------------------|------------|----------------------------------|
| `sw a0, 0(a1)`       | `00a52023` | Store word from a0 into [a1]     |
| `sb a0, 0(a1)`       | `00a50023` | Store byte from a0 into [a1]     |
| `sh a0, 0(a1)`       | `00a51023` | Store halfword from a0 into [a1] |

---

## 📕 B-Type Instructions

| Instruction             | Encoding   | Description                      |
|-------------------------|------------|----------------------------------|
| `beq a0, a1, label`      | `00b50663` | Branch if a0 == a1               |
| `bne a0, a1, label`      | `00b51663` | Branch if a0 ≠ a1                |
| `blt a0, a1, label`      | `00b51463` | Branch if a0 < a1                |

---

## 📘 U-Type Instructions

| Instruction          | Encoding   | Description                      |
|----------------------|------------|----------------------------------|
| `lui a0, 0x12345`     | `12345037` | Load upper 20 bits into a0       |
| `auipc a0, 0x12345`   | `12345017` | Add upper immediate to PC        |

---

## 📗 J-Type Instruction

| Instruction         | Encoding   | Description                      |
|---------------------|------------|----------------------------------|
| `jal a0, label`      | `000000ef` | Jump to label, store return addr |

---

## 📸 Screenshots

All disassembled outputs (objdump) are saved under `/screenshots/` for visual reference. Each image includes:

- Instruction hex encoding  
- Disassembled output  
- Register usage breakdown  

---

## 🚀 How These Were Generated

Each instruction was written in `.s` assembly source files, assembled using:

```bash
riscv64-unknown-elf-as <file>.s -o <file>.o
riscv64-unknown-elf-objdump -d <file>.o
