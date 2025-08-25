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
|1200:12                  | 24:1204                  |
|1201:34                  | 68:1205                  |
|1202:12                  | 00:1206                  |
|1203:34                  | C4:1207                  |

#### Manual Calculations

(Add your calculation here)

![WhatsApp Image 2025-08-24 at 20 42 48_ca04df0c](https://github.com/user-attachments/assets/2dca94a7-67b1-4791-8a60-8c7bcfd6c96b)


## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="640" height="480" alt="Screenshot (324)" src="https://github.com/user-attachments/assets/f4ff21b1-8ebd-472d-b973-8abaf97fa5f4" />



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
|1200:12                  | 00:1204                  |
|1201:34                  | 00:1205                  |
|1202:12                  | 83:1206                  |
|1203:34                  | C4:1207                  |


#### Manual Calculations

(Add your calculation here)

![WhatsApp Image 2025-08-24 at 20 40 23_7accbcaa](https://github.com/user-attachments/assets/c74711a6-f1ce-4178-abfb-6f1b07687ae5)



## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="640" height="480" alt="Screenshot (330)" src="https://github.com/user-attachments/assets/9a8ab4e7-f833-485c-a101-2be2e81ed126" />

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
|1200:12                  | 44:1204                  |
|1201:34                  | 51:1205                  |
|1202:12                  | 97:1206                  |
|1203:34                  | 0A:1207                  |
                         

#### Manual Calculations

(Add your calculation here)

![WhatsApp Image 2025-08-24 at 20 41 53_242fd617](https://github.com/user-attachments/assets/5bf4af69-795a-4c2e-9621-9e292a4b60e7)


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (335)" src="https://github.com/user-attachments/assets/a4671797-9ce9-4db8-8e15-9e4a45efd59b" />

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
|1200:12                  | 01:1204                  |
|1201:34                  | 00:1205                  |
|1202:12                  | 00:1206                  |
|1203:34                  | 00:1207                  |
                                                            

#### Manual Calculations

(Add your calculation here)

![WhatsApp Image 2025-08-24 at 20 44 55_cade4027](https://github.com/user-attachments/assets/dfc96d38-c190-41fd-afb9-4f1eea1b91e8)

## OUTPUT FROM MASM SOFTWARE

<img width="640" height="480" alt="Screenshot (333)" src="https://github.com/user-attachments/assets/8777aed0-276b-40ae-80ce-e12c23df7791" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written  and executed using MASM.
