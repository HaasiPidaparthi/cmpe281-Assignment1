# CMPE 281 Assignment 1

Haasitha Pidaparthi

## Procedure

### Setup Environment
* Download and Install VMware Fusion 12 Pro for MacOS.
* Download latest Ubuntu Desktop (Ubuntu 20.04.1 LTS) ISO image.
* Create a custom virtual machine using Linux Ubuntu 64-bit operating system and the disk image downloaded in the previous step.
* Allocate 250 GB storage space with 4 GB RAM.
* Under CPU Settings, enable nested virtualization for the virtual machine. 
Run the VM. Verify that nested virtualization is enabled by using the command **cat /proc/cpuinfo | more**  in the terminal.

### Steps used for this assignment
* Install Github: sudo apt-get install git
* Clone the Linux repository: git clone https://github.com/torvalds/linux.git
* Use the command **ls -latr** to check all the files installed from git.
* Build the code by using the command **make**
* After we build the code, use the command **ls -latr .**  and check for the file named “cmpe283-1.ko”. This is the kernel object we will load into the kernel.
* Use the command **sudo insmod ./cmpe283-1.ko** followed by **dmesg** to display the output. 
* In this stage, the module is already loaded into kernel. So, to rerun the file, simply remove the mod and install it again using the following commands 
    * **sudo rmmod cmpe283-1.ko**
    * **sudo insmod ./cmpe283-1.ko**
    * **dmesg**
