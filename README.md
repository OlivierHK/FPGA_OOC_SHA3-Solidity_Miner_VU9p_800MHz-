# FPGA_OOC_SHA3-Solidity_Miner_VU9p_800MHz-
An optimized VHDL bottom-up OOC Implementation of the SHA3-Solidity (800MHz Clock frequency) mining algorithm for Virtex Ultrascale+ VU9p for Alto UltraP platform. 

## Summary

This Project is using same VHDL code as [FPGA_Monolithic_SHA3-Solidity_Miner_VU9p_600MHz](https://github.com/OlivierHK/FPGA_Monolithic_SHA3-Solidity_Miner_VU9p_600MHz), but is built in a totally different way:


1. The project is fully build with via Tcl scripting. No Vivado GUI involved.
2. Core frequency is closing timing at 800MHz, and MMCM frequency can be increased up to 1GHz.
3. Every Core get Synth/Impl independantly, using OOC (Out-Of-Context) design and a complete set of dedicated constraint files (Timing & Floorplanning). Placement and routing then get Locked.
4. Top Project is then built Bottom-up by either TcL scripting, or by using [RapidWright](https://github.com/Xilinx/RapidWright) for stitching the cores to the top-Level design.


## Code & Scritping

This project is still under construction and evaluation. For Code & Script, please e-mail the author at olivier.faurie.hk@gmail.com.
