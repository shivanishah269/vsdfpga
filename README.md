# RVMYTH_PLL
This repository explains the implementation of Mixed Signal SoC (RISCV based Core + PLL) on FPGA.

# Installtion and Overview of Sandpiper
* [SandPiper](https://www.redwoodeda.com/products) is a code generator that generates readable, well-structured, Verilog or SystemVerilog code from the given TL-Verilog code.
* [SandPiper SaaS Edition](https://pypi.org/project/sandpiper-saas/) runs as a microservice in the cloud to support easy open-source development. Install Sanpiper SaaS Edition for this project. 
* To run locally, SandPiper Education Edition can be requested from [RedwoodEDA](https://www.redwoodeda.com/products)

# Steps to convert TL-Verilog to Verilog or SystemVerilog

1. Install Sandpiper SaaS (https://pypi.org/project/sandpiper-saas/)
2. `git clone https://github.com/shivanishah269/RVMYTH_PLL.git`
3. `cd vsdfpga/verilog`
4. ` sandpiper-saas -i rvmyth_updated.tlv -o rvmyth_updated.v --iArgs`

# Steps for RTL Simulation of RVMYTH+PLL using iverilog

1. `iverilog iverilog rvmyth_pll_tb.v rvmyth_pll.v clk_gate.v`
2. `./a.out`
3. `gtkwave rvmyth_pll.vcd`
