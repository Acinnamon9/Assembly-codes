
### Example: "Hello, World!" in x86 Assembly (Linux)

```asm
section .data
    hello db 'Hello, World!', 0xA  ; The string to print (with a newline character)
    hello_len equ $ - hello         ; Length of the string

section .text
    global _start                   ; Entry point for the program

_start:
    ; Write the string to stdout
    mov eax, 4                      ; syscall number for sys_write (4)
    mov ebx, 1                      ; file descriptor 1 (stdout)
    mov ecx, hello                  ; pointer to the string
    mov edx, hello_len              ; length of the string
    int 0x80                        ; make the syscall

    ; Exit the program
    mov eax, 1                      ; syscall number for sys_exit (1)
    xor ebx, ebx                    ; exit code 0
    int 0x80                        ; make the syscall
```
