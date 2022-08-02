# JS 8086 Intel Processor Assembly Emulator

## MOV destination, source
### Instruction Regulations <br />
  - if source is a number we put it directly in the source(memory location or register with taking the size into consideration).
  ```asm
  mov ax, 16
  ```
  - if source if a single quoted letter/number the emulator treats it as hex value.
  ```asm
  mov bx, 'A'
  ```
  - if the source is a string we have two cases:
      - if we are storing the source in a register, then the string length must be equals to 2.
      ```asm
      mov dx, 'Hi'
      ```
      - if we storing the source in memory, each caracter gets stored in a memory location in a consecutive manner.
      ```asm
      mov [12563], 'Hello world!'
      ```
