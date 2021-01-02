---
layout: post
title:  "Raspberry Pi"
date:   2020-11-15 18:09:00 +0700
categories: jekyll update
---
    https://www.cl.cam.ac.uk/projects/raspberrypi/tutorials/
    https://www.valvers.com/open-software/raspberry-pi/bare-metal-programming-in-c-part-1/
    https://azeria-labs.com/emulate-raspberry-pi-with-qemu/
    https://wiki.qemu.org/Documentation/Platforms/ARM


Start qemu:

    ./qemu-system-arm -s -S -m 512 -M raspi1ap -serial stdio -kernel /home/mih/projects/Raspberry/bare-metal-pi/output/rasppi.elf
