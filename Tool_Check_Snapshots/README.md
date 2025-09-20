# 🖥️ RISC-V Reference SoC Tapeout Program (VSD)

## 📌 Introduction  

This guide walks you through the installation of essential FPGA/ASIC design and verification tools — **Yosys**, **Icarus Verilog**, and **GTKWave** — on an Ubuntu Linux system.  

---

## 🎯 Objective  

The aim of this document is to help you set up and configure key open-source tools for FPGA and ASIC workflows on a Linux environment.  

By the end of this setup, you’ll be able to:  

- Design and develop HDL/RTL modules  
- Run simulations and functional verification  
- View and analyze waveforms with GTKWave  
- Streamline your FPGA and ASIC design process  

---

## 🔧 Tools Covered  

- **Yosys 🟢** – Open-source synthesis tool for Verilog  
- **Icarus Verilog (Iverilog) 🔵** – Verilog simulation and synthesis tool  
- **GTKWave 🟣** – Waveform viewer for simulation results  

Together, these tools create a complete open-source HDL design and verification environment.  

---

## ⚙️ System Requirements  

Make sure your system meets at least the following specs to ensure smooth installation and operation:  

- 💾 **RAM:** 6 GB or more (for compiling/simulating larger HDL designs)  
- 📂 **Storage:** 50 GB HDD free (for tools, libraries, and simulation files)  
- 🐧 **OS:** Ubuntu 20.04 or newer (full compatibility)  
- ⚡ **CPU:** 4 vCPUs or more (faster synthesis, simulation, waveform processing)  

---

## 🛠️ Tool Check & Installation  

### Yosys  

```bash
sudo apt-get update
git clone https://github.com/YosysHQ/yosys.git
cd yosys
sudo apt install make    # If make is not installed
sudo apt-get install build-essential clang bison flex \
  libreadline-dev gawk tcl-dev libffi-dev git \
  graphviz xdot pkg-config python3 libboost-system-dev \
  libboost-python-dev libboost-filesystem-dev zlib1g-dev

make config-gcc

# Initialize abc submodule before building
git submodule update --init --recursive

make
sudo make install
```

✅ **Yosys installed successfully**  



### Icarus Verilog  

```bash
sudo apt-get update
sudo apt-get install iverilog
```

✅ **Icarus Verilog installed successfully**  

---

### GTKWave  

```bash
sudo apt-get update
sudo apt install gtkwave
```

✅ **GTKWave installed successfully**  

---

## 📝 Conclusion  

You’ve successfully installed **Yosys**, **Icarus Verilog**, and **GTKWave**.  
With this setup, you now have a complete open-source environment for:  

- HDL design  
- RTL synthesis  
- Functional simulation  
- Waveform analysis  

This toolchain empowers efficient FPGA and ASIC development workflows. 🚀  
````
