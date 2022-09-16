1. Download eos2022.tgz

2. Under Ubuntu Linux, run

         zcat eos2022.tgz | tar xvf -

   to extract files, which are organized by Chapters.

3. eos2022.tgz contains the following enhancements:

3.1. In Ubuntu 15.10-16.04, ARM emulator in QEMU uses scan code keyset 1.
     In Ubuntu 18-20, it uses scan code keyset 2.
     The keyboard drivers are updated to handle both cases.
    
3.2. Loading ELF executable image files is too hard for students.
     In ch7.load, the loader loads flat binary image files.

3.3. In ch6, ch7 and ch8, when kerenl uses High VA at 2GB (0x80000000), 
     the vector table is remapped to the highest 64KB in a 1MB section.
     The highest 1MB VA is mapped to that 1MB section.
     The remapped vector table is at VA=0xFFFF0000
     The VA space of Umode images begin at VA=0

NOTE: The SDC driver has been updated. 
      It now works for QEMU Arm Virtual Machines in Ubuntu 18.10 to 20.04

Enjoy and have fun

KCW
kwang@eecs.wsu.edu