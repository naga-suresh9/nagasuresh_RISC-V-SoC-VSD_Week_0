# 🖥️ VSD RISC-V Reference SoC Tapeout Program  

## 📍 Overview  

This handbook provides a clear, step-by-step process to install the core open-source FPGA/ASIC design and verification tools — **Yosys**, **Icarus Verilog**, and **GTKWave** — on Ubuntu Linux.  

---

## 🎯 Goal  

Set up a ready-to-use environment for digital design and verification.  
After completing this setup you’ll be able to:  

- Write and develop HDL/RTL code  
- Perform simulation and functional checks  
- Visualize results with GTKWave  
- Streamline FPGA/ASIC workflows using open-source tools  

---

## 🔧 Toolkit  

| Tool | Purpose |
|------|---------|
| **Yosys 🟢** | Verilog synthesis (open-source) |
| **Icarus Verilog 🔵** | Verilog simulation/synthesis |
| **GTKWave 🟣** | Waveform viewing and analysis |

These tools together form a complete HDL design + verification environment.  

---

## ⚙️ Recommended System Specs  

Before installing, make sure your system meets these minimum requirements:  

- 💾 **RAM:** 6 GB or more (smooth compilation and simulation)  
- 📂 **Disk Space:** 50 GB free for tools and simulation data  
- 🐧 **OS:** Ubuntu 20.04 or newer  
- ⚡ **CPU:** Quad-core or more for faster builds  

---

## 🛠 Installation Steps  

### 1️⃣ Yosys  

```bash
sudo apt-get update
git clone https://github.com/YosysHQ/yosys.git
cd yosys
sudo apt install make    # if make not installed

sudo apt-get install build-essential clang bison flex \
  libreadline-dev gawk tcl-dev libffi-dev git \
  graphviz xdot pkg-config python3 libboost-system-dev \
  libboost-python-dev libboost-filesystem-dev zlib1g-dev

make config-gcc

# Initialize abc submodule before build
git submodule update --init --recursive

make
sudo make install
```

✅ **Yosys installed successfully**  

![Image](https://github.com/user-attachments/assets/dffc719b-ec28-4954-a1e4-bdaa4a700b0c)

### 2️⃣ Icarus Verilog  

```bash
sudo apt-get update
sudo apt-get install iverilog
```

✅ **Icarus Verilog installed successfully**  

---

### 3️⃣ GTKWave  

```bash
sudo apt-get update
sudo apt install gtkwave
```

✅ **GTKWave installed successfully**  

---

## 🚀 Wrap-Up  

With **Yosys**, **Icarus Verilog**, and **GTKWave** now installed, you have a complete open-source flow for:  

- HDL/RTL design  
- Synthesis  
- Simulation  
- Waveform analysis  

This lightweight toolchain enables efficient FPGA and ASIC development from your Ubuntu system.  
````
