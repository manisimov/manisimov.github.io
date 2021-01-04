---
layout: post
title:  "Raspberry Pi"
date:   2020-11-15 18:09:00 +0700
categories: jekyll update
---
# This post is about Raspberry Pi Model B+.

    https://www.cl.cam.ac.uk/projects/raspberrypi/tutorials/
    https://www.valvers.com/open-software/raspberry-pi/bare-metal-programming-in-c-part-1/
    https://azeria-labs.com/emulate-raspberry-pi-with-qemu/
    https://wiki.qemu.org/Documentation/Platforms/ARM


# QEMU:

    ./qemu-system-arm -s -S -m 512 -M raspi1ap -serial stdio -kernel /home/mih/projects/Raspberry/bare-metal-pi/output/rasppi.elf
    
# Interrupts:

Interrupt vectors are not loaded by bootloader, because they are at 0x00000000, and bootloader loads kernel image to 0x00008000. Vectors must be copied to 0x0 at runtime.

QEMU behaves differently and doesn't have this issue. It copies .text section of the elf file, which contains address information and can serve as the source of the interrupt vectors table.

    https://www.valvers.com/open-software/raspberry-pi/bare-metal-programming-in-c-part-4/
