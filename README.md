# Linux-world (h1)
This repo is all about Linux pods and nodes 
Part I- “Power ON” to “Loading Kernel”

## Overview of Part 1: 

<small>This text will be smaller.</small>
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
[Ansible code.txt](https://github.com/user-attachments/files/19869333/Ansible.code.txt)

Repo to learn Docker with examples. Contributions are most welcome.
If you found this repo useful, give it a STAR 🌠

You can watch the video version of this repo on my youtube playlist. -> https://www.youtube.com/watch?v=7JZP345yVjw&list=PLdpzxOOAlwvLjb0vTD9BXLOwwLD_GWCmC
What is a container ?

A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries and settings.

Ok, let me make it easy !!!

A container is a bundle of Application, Application libraries required to run your application and the minimum system dependencies.
