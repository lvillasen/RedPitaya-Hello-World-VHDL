# RedPitayaHelloWorldVHDL
Hello World code in VHDL for the RedPitaya board

Luis Villaseñor

License: GPLv3

Date: 2016-03-11

Updated: 2022-08-13



# Usage

Create a new project with Vivado (tested with Vivado v2019.1) 

see https://www.xilinx.com/support/download.html

Add the vrilog and the xdc files provides according to the block design shown in the screenshot provided. 

Proceed to run Synthesis, Implementation and Bitstream Generation

Find the bitstream file (you may use the command 'find . -name *bit')

Transfer the bitstream file generated (*.bit)  to the Red Pitaya (you may use sftp root@rp-ip) type

cat file_name.bit > /dev/xdevcfg

The 8-bit LEDs will display a binary incremental counter at a rate of 1Hz

You may change the clock rate by editing the verilog counter module provided.

Reboot the Red Pitaya board to reinstall the permanent bitstream on the Zynq FPGA

