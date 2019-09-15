---
title: Use ZFS in Tiny Core Linux
---

ZFS is a combined file system and logical volume manager designed by Sun Microsystems. ZFS is scalable, and includes extensive protection against data corruption, support for high storage capacities, efficient data compression, integration of the concepts of filesystem and volume management, snapshots and copy-on-write clones, continuous integrity checking and automatic repair, RAID-Z, native NFSv4 ACLs, and can be very precisely configured. (From Wikipedia)


Tiny Core Linux does not offer an official ZFS tcz. You can use the script in https://github.com/hpmtissera/zfs-tinycore to build a ZFS TCZ file for Tiny Core. By default it will build Tiny Core:10.0-x86_64 (Kernel: 4.19.10-tinycore64). But you can change the base image version (https://github.com/hpmtissera/zfs-tinycore/blob/master/Dockerfile#L1) and kernel version (https://github.com/hpmtissera/zfs-tinycore/blob/master/Dockerfile#L29) in the Dockerfile to build ZFS for the required version.
