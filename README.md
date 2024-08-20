# Assembly-codes
How to Assemble and Link:
To run this code on a Linux machine:

Save the code to a file, say hello.asm.

Assemble the code using NASM:

bash
Copy code
nasm -f elf32 hello.asm -o hello.o
Link the object file to create an executable:

bash
Copy code
ld -m elf_i386 -s -o hello hello.o
Run the executable:

bash
Copy code
./hello
You should see "Hello, World!" printed in the terminal.

Note from the developer: WSL provides linux kernel on windows and it smoothly integrates with vs code. Highly recommended to download and fiddle it with.
