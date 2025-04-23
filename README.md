# Linux-world
This repo is all about Linux pods and nodes 
Part I- “Power ON” to “Loading Kernel”

Overview of Part 1: 
**Step** 1- BIOS or UEFI firmware loads first
When we power the PC, the BIOS (stored on the Motherboard) loads into RAM. The purpose of BIOS is to load the Operating System or Kernel into RAM.

**Step 2-
**BIOS searches for a Bootable Device. When a bootable device is found, it goes to the next step.

Step 3- **Bootloader**
When a bootable device is found, it loads  1-stage Bootloader, i.e., MBR, into RAM. The size of the MBR is just 512 bytes. Just the first sector of the Hard disk.

**Step 4- **
The first stage bootloader loads the Second stage bootloader, i.e., GRUB (GRand Unified Bootloader) or LILO.

Step 5- Kernel
When the second-stage bootloader is executed in RAM, the Splash Screen is displayed. The job of the second-stage bootloader is to load the kernel (/boot/vmlinuz-*) into RAM.

Step 6-
Stage 2 bootloaders load the Kernel and optional initial Root Filesystem into RAM. It passes control to the Kernel, and the kernel gets decompressed into RAM and initialized. At this stage, the second-stage bootloader checks hardware, mounts the root device, and loads necessary kernel modules. The first User space program is executed when it is complete, i.e., [/sbin/init.] Init (system) is the father of all processes.
