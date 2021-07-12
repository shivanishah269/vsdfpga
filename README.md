# vsdfpga
This repository explains the implementation of Mixed Signal SoC (RISC-V based Core + PLL) on FPGA.

__MYTH Core:__ https://github.com/shivanishah269/risc-v-core

__PLL:__ https://github.com/vsdip/rvmyth_avsdpll_interface

# Tools used:

__Makerchip:__  

[Makerchip](https://www.makerchip.com/) is a free web-based IDE as well as available as [makerchip-app](https://gitlab.com/rweda/makerchip-app), a virtual desktop application for developing high-quality integrated circuits. You can code, compile, simulate, and debug Verilog designs, all from your browser. Your code, block diagrams, and waveforms are tightly integrated.

__Icarus Verilog:__

[_Icarus Verilog_](http://iverilog.icarus.com/) is a Verilog simulation and synthesis tool.

__GTKWave:__

[GTKWave](http://gtkwave.sourceforge.net/) is a waveform viewer.

__Xilinx Vivado:__

[Xilixn Vivado](https://www.xilinx.com/support/university/vivado.html) provides complete SoC-strength, IP-centric and system-centric, next generation development environment. Currently, this project is done using Vivado HL Design Edition 2019.1.

# FPGA board used:
Zedboard Zynq-7000 ARM/FPGA SoC Development Board ([Product Link](https://www.avnet.com/wps/portal/us/products/avnet-boards/avnet-board-families/zedboard/))

![image](https://user-images.githubusercontent.com/15063738/125192735-f9c65b80-e266-11eb-9130-799199fa208a.png)


# Installtion and Overview of Sandpiper
* [SandPiper](https://www.redwoodeda.com/products) is a code generator that generates readable, well-structured, Verilog or SystemVerilog code from the given TL-Verilog code.
* [SandPiper SaaS Edition](https://pypi.org/project/sandpiper-saas/) runs as a microservice in the cloud to support easy open-source development. Install Sanpiper SaaS Edition for this project. 
* To run locally, SandPiper Education Edition can be requested from [RedwoodEDA](https://www.redwoodeda.com/products)

# Steps to convert TL-Verilog to Verilog or SystemVerilog

1. Install Sandpiper SaaS (https://pypi.org/project/sandpiper-saas/)
2. `git clone https://github.com/shivanishah269/vsdfpga.git`
3. `cd vsdfpga/verilog`
4. ` sandpiper-saas -i rvmyth.tlv -o rvmyth.v --iArgs`

# Steps for RTL Simulation of RVMYTH+PLL using iverilog

1. `iverilog rvmyth_pll_tb.v rvmyth_pll.v clk_gate.v`
2. `./a.out`
3. `gtkwave rvmyth_pll.vcd`

# Acknowledgements
- [Kunal Ghosh](https://github.com/kunalg123), Co-founder, VSD Corp. Pvt. Ltd.
- [Steve Hoover](https://github.com/stevehoover), Founder, Redwood EDA
