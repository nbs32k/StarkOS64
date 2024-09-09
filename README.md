# StarkOS64
An x86 64-bit operating system designed by researching NT's kernel and therefore following NT operating systems architecture.

The kernel and the disk driver are loaded by a custom 32-bit bootloader called NT loader that is able to manage memory and switch modes.\
All components are fully compatible with MSVC compiler and NASM.

#### Memory layout
```
0xffff800000000000 - 0xffff8??????????? Mirror mapped free memory
0xffff900000000000 - 0xffff9??????????? Page frame number database
0xfffff00000000000 - 0xfffff000000d0000 Stack, BIOS, VGA/VESA etc.
0xfffff80000000000 - 0xfffff8?????????? Kernel executable code (kernel itself, drivers etc.)
0xfffffa0000000000 - 0xfffffb0000000000 Non paged pool area
0xfffffc0000000000 - 0xfffffd0000000000 Paged pool area
0xffffff0000000000 - 0xffffff0000001000 System's page directory
```

![image](https://github.com/user-attachments/assets/940dd192-25e3-41ad-bf78-56836d364345)
