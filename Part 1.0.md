First you will need nasm installed on your machine to compile it.

sudo apt-get install nasm

![](https://user-images.githubusercontent.com/43363015/78869653-854cad80-7a62-11ea-8a56-9d9878298959.PNG)

Write the below assembly code in an editor and save as shell.asm

![](https://user-images.githubusercontent.com/43363015/78870985-9f878b00-7a64-11ea-91d2-f405fbc7f4cf.PNG)

To compile it use the following commands

$nasm -f elf -o shell.o shell.asm

$ld -o shell shell.o

![](https://user-images.githubusercontent.com/43363015/78871250-0e64e400-7a65-11ea-99dc-dd9664d89905.PNG)

To address this issue we can use the following commands

$nasm -f elf64 -o shell.o shell.asm 

$ld -m elf_x86_64 -s -o shell shell.o

Now run it with:

./shell

![](https://user-images.githubusercontent.com/43363015/78871874-0194c000-7a66-11ea-84b6-eed5d79c25e5.PNG)
