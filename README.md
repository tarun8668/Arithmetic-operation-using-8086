# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|     2000 : 12           |      2004 : 68           |
2001 : 34  |  2005 : 24
2002 : 12   | 2006 : 00
2003 : 34    |2007 : C4

#### Manual Calculations

![WhatsApp Image 2025-08-26 at 11 07 20_b56546aa](https://github.com/user-attachments/assets/2bbbecfe-d3b7-47b2-9117-bd80f3ace381)



---

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="641" height="423" alt="image" src="https://github.com/user-attachments/assets/1665c5f2-6c38-42f8-9bfa-79156a50fa4b" />



## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|               2000 : 12          |      2004 : 00                    |
2001 : 34 | 2005 : 00
2002 : 12 | 2006 : 00
2003 : 34 | 2007 : C4

#### Manual Calculations

![WhatsApp Image 2025-08-26 at 11 09 03_87498700](https://github.com/user-attachments/assets/360f2f8d-f6e0-47c9-bf96-bb9a958233ad)




---


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="636" height="427" alt="image" src="https://github.com/user-attachments/assets/77512551-29b2-48f3-9cb7-c25813665f8c" />



## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         2000 : 12                |       2004 : 44                   |
2001 : 34 | 2005 : 51
2002 : 12 | 2006 : 97
2003 : 34 | 2007 : 0A

#### Manual Calculations

![WhatsApp Image 2025-08-26 at 11 26 07_e75eaa1a](https://github.com/user-attachments/assets/0920ed19-94fd-42c2-b8e0-fd8e67bf4aa3)



---

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="643" height="392" alt="image" src="https://github.com/user-attachments/assets/a42514d2-9f4e-43f1-8bcb-86c419407e9c" />



## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       2000 : 34                  |              2004 : 01            |
2001 : 12 | 2005 : 00
2002 : 34 | 2006 : 00
2003 : 12 | 2007 : 00

#### Manual Calculations

![WhatsApp Image 2025-08-26 at 11 31 14_d4d92edf](https://github.com/user-attachments/assets/e91db3d5-5204-43e3-8a2c-2b37c73f978b)




---
## OUTPUT FROM MASM SOFTWARE

<img width="637" height="402" alt="image" src="https://github.com/user-attachments/assets/794bd0d4-4d79-4465-89e6-3439795d4e7f" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
