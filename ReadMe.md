# MinLin.Kernel

Linux Kernel for MinLin, specialized for NanaBox virtual machines, but standard
Hyper-V virtual machines is supported.

If you are looking for the history of kernel configurations, have a look at
https://github.com/SherryPlatform/MinLin.Kernel.Configurations.

# Build Instructions

Instructions for building an x86_64 MinLin.Kernel kernel with an Debian-based 
distribution are as follows:

## Install the build dependencies:  

`$ sudo apt install build-essential flex bison dwarves libssl-dev libelf-dev`

## Build the kernel from one of the flavors which you wanted:

### Hyper-V Generation 2 Virtual Machines

You can choose these configurations for Azure, Hyper-V and NanaBox.

Note: NanaBox is a third-party lightweight XAML-based out-of-box-experience 
oriented Hyper-V virtualization software based on Host Compute System API, 
Remote Desktop ActiveX control and XAML Islands, project repository available
at https://github.com/M2Team/NanaBox. NanaBox is the reference and prototype
virtualization platform for MinLin.

- x64, generic, as modularized as possible
  `$ make KCONFIG_CONFIG=MinLin/config-x64-NanaBox`
- x64, generic, make essential modules builtin
  `$ make KCONFIG_CONFIG=MinLin/config-x64-NanaBox.Medium`
- x64, generic, make all modules builtin
  `$ make KCONFIG_CONFIG=MinLin/config-x64-NanaBox.Single`
- arm64, generic, as modularized as possible
  `$ make KCONFIG_CONFIG=MinLin/config-arm64-NanaBox`
- arm64, generic, make essential modules builtin
  `$ make KCONFIG_CONFIG=MinLin/config-arm64-NanaBox.Medium`
- arm64, generic, make all modules builtin
  `$ make KCONFIG_CONFIG=MinLin/config-arm64-NanaBox.Single`
