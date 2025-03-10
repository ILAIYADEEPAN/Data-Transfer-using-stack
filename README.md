# DATA TRANSFER USING STACK
## Theory
# Stack in Assembly
The stack is a section of memory used for temporary storage. It operates in a LIFO (Last In, First Out) manner. The SP (Stack Pointer) register manages the stack.

#  Instructions Used
PUSH → Stores a value into the stack.
POP → Retrieves the last value stored in the stack.
MOV → Transfers data between registers.
CALL/RET → Used for function calls (not used in this basic example).
Data Transfer Using Stack
Data is pushed onto the stack from registers.
The stack pointer (SP) adjusts accordingly.
Data is then popped into another register for processing or transfer.

# Diagram
![workshop](https://github.com/user-attachments/assets/df5473bd-fed2-47a0-87ae-0210560f634a)



# Program:
~~~
MOV AX, BX
PUSH AX
POP BX
IN AL, 60H
OUT 70H, AL
HLT
~~~
# Output:
![Screenshot (145)](https://github.com/user-attachments/assets/4c54a317-d27b-4940-b827-cb1a9986c610)


# Program Flow:
~~~
MOV AX, BX → AX gets BX’s value.
PUSH AX → AX value is saved on the stack.
POP BX → BX retrieves the last pushed value (AX).
IN AL, 60H → Reads a value from port 60H (keyboard).
OUT 70H, AL → Sends that value to port 70H (RTC).
HLT → Stops execution.
~~~


