# Task 1 - RISC-V Design and Simulation

This task involves setting up the RISC-V toolchain and verifying a simple design using the following tools:

- Yosys
- GTKWave
- IVerilog
- RISCV toolchain

---
# 🧠 Task 1 - RISC-V Toolchain Setup & Simulation

This task covers setting up the RISC-V design environment and running simulation using open-source tools on Ubuntu.

---


## 🔧 Tool Installation Screenshots

### ✅ RISC-V Toolchain Installation
![RISC-V Toolchain](riscv_toolchain.png)
git clone https://github.com/riscv-collab/riscv-gnu-toolchain
cd riscv-gnu-toolchain
sudo apt install autoconf automake autotools-dev curl libmpc-dev libmpfr-dev libgmp-dev gawk build-essential bison flex texinfo gperf libtool patchutils bc zlib1g-dev libexpat-dev
./configure --prefix=/opt/riscv
make


### ✅ Ubuntu Installed
![Ubuntu Installed](ubuntu_installed.png)

---

## 🧪 Waveform Output

### ✅ GTKWave Output
![GTKWave](gtkwave.png)
## 🔧 Toolchain Components

GTKWave is a waveform viewer for VCD (Value Change Dump) files generated from simulations.
sudo apt install gtkwave


### ✅ xdot View
![xdot](xdot.png)

---

## ⚙️ Synthesis and Simulation

### ✅ Yosys Synthesis Output
![Yosys](yosys.png)

## 🔧 Toolchain Components

### 1. **Yosys**
> Yosys is an open-source framework for Verilog RTL synthesis.

📌 **Command Used:**
```bash
sudo apt install yosys


### ✅ IVerilog Compilation
![IVerilog](iverilog.png)

## 🔧 Toolchain Components

Icarus Verilog (IVerilog) is a Verilog simulation and synthesis tool.
sudo apt install iverilog


