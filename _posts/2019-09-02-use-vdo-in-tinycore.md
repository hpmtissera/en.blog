---
title: Use Redhat VDO in Tiny Core Linux
---

Virtual Data Optimizer (VDO) is a compression/deduplication layer developed by Redhat. [https://www.redhat.com/en/blog/look-vdo-new-linux-compression-layer](https://www.redhat.com/en/blog/look-vdo-new-linux-compression-layer)


To use VDO in Tiny Core we need to install both KVDO and VDO TCZs. KVDO contains the kernel modules. 


Tiny Core does not have an official KVDO or VDO TCZs. KVDO does not work with the default Tiny Core 10.x distribution. It is necessary to build a Tiny Core Kernel with custom configurations. 



The build.sh script in [https://github.com/hpmtissera/tinycore-kernel-build.git](https://github.com/hpmtissera/tinycore-kernel-build.git) can be used to build Tiny Core Kernel with suitable configurations for VDO. After the build is completed generated vmlinuz64, corepure64 and other kernel components copied to the kernel-artifacts folder should be used instead of the defaults from http://tinycorelinux.net/10.x/x86_64/release/.



To build KVDO use the build.sh script in [https://github.com/hpmtissera/kvdo-tinycore.git](https://github.com/hpmtissera/kvdo-tinycore.git). You can use the build.sh script in [https://github.com/hpmtissera/vdo-tinycore](https://github.com/hpmtissera/vdo-tinycore) to build Redhat VDO.  


By default, these scripts will build TCZs for Tiny Core:10.0-x86_64 (Kernel: 4.19.10-tinycore64). Also, note that you need to use "depmod" command to load kernel modules after installing KVDO TCZ. 

A TCZ for Python Yaml module is included in vdo-tinycore. This python3.6-yaml.tcz and python3.6.tcz are required dependecies for vdo.tcz. (Please note that there can be few other trivial dependencies)
