
# Boot sequence
1. **ROM BIOS**

 boot.s is loaded at 0x7c00 by the bios-startup routines
1. **/boot/boot.S**

 moves itself out of the way to address 0x90000, and 

 jumps there.

 It then loads the system at 0x10000, using BIOS interrupts. 

 Thereafter it disables all interrupts, 

 moves the system down to 0x0000, 

 changes to protected mode, and 

 calls the start of system. 

1. **/init/main.c**

 System then must RE-initialize the protected mode in it's own tables, 

 and enable interrupts as needed.




sources:

http://www.tldp.org/LDP/khg/HyperNews/get/tour/tour.html

the code itself
