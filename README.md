# Skill assessment - 1

## AIM
Write an assembly language program in 8051 to find the largest number from a given set of N numbers stored in memory. Display the result in AL register.

## APPARATUS REQUIRED
- Personal Computer  
- Keil µVision Software  

## PROGRAM


```
ORG 0000H
iMOV R0, #30H
MOV R1, #05H
MOV A, @R0
INC R0
DEC R1
LOOP: MOV B, @R0
      CJNE A, B, CHECK
      SJMP NEXT
CHECK: JNC NEXT     
       MOV A, B     
NEXT: INC R0
      DJNZ R1, LOOP
MOV P1, A           
HERE: SJMP HERE
END
```

### OUTPUT:

<img width="1919" height="1144" alt="Screenshot 2025-10-24 212854" src="https://github.com/user-attachments/assets/a6105bf6-5540-4330-a729-d3d6fda835dc" />

### RESULT:
Thus the largest number from a given set of N numbers stored in memory and displayed the result in AL register.
