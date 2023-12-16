# MinLin.Kernel

Linux Kernel for MinLin, specialized for NanaBox virtual machines, but standard
Hyper-V virtual machines is supported.

# Build Instructions

Instructions for building an x86_64 WSL2 kernel with an Ubuntu distribution are
as follows:

1. Install the build dependencies:  
   `$ sudo apt install build-essential flex bison dwarves libssl-dev libelf-dev`
2. Build the kernel using the WSL2 kernel configuration:  
   `$ make KCONFIG_CONFIG=MinLin/config-MinLin.Kernel.NanaBox`
