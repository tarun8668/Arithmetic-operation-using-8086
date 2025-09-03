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
|  1200:12                |                  1204:24 |
|  1201:34                |                  1205:68 |
|  1202:12                |                          |
|  1203:34                |                          |

#### Manual Calculations

(Add your calculation here)

---![IMG-20250830-WA0002 1](https://github.com/user-attachments/assets/b6bde718-d2b7-4bd3-bdba-87a71beeb31f)


## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="633" height="431" alt="image" src="https://github.com/user-attachments/assets/32f20509-f45e-41de-8449-2b2dd58f0e32" />

<img width="621" height="422" alt="image" src="https://github.com/user-attachments/assets/0fb28922-6203-4bad-9e2b-e52205481778" />





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
```
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,O0H
MOV AX, [SI]
MOV BX, [SI+02H]
SUB AX, BX
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
|    1200:12               |  1204:00                 |
|   1201:34               |  1205:00                 |              
|   1202:12               |                          |
|   1203:34              |                          |

#### Manual Calculations

(Add your calculation here)

---![IMG-20250830-WA0001 1](https://github.com/user-attachments/assets/74782ca9-d519-4e36-95b2-9d8630b7a1a0)


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="632" height="436" alt="image" src="https://github.com/user-attachments/assets/21899f47-da77-417f-962d-30f756e0b76e" />


<img width="890" height="427" alt="image" src="https://github.com/user-attachments/assets/c1b22fe8-8a65-4001-a217-5db87a0d5c43" />




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
|   1200:12              |  1204:44                 |
|   1201:34               |  1205:51                 |              
|   1202:12               |  1206:97                 |
|   1203:34               |  1207:0A                 |

#### Manual Calculations

(Add your calculation here)

---<img width="711" height="576" alt="image" src="https://github.com/user-attachments/assets/59afaac2-8ee4-4a7a-b3e0-a02217a2be28" />

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="637" height="426" alt="image" src="https://github.com/user-attachments/assets/c7b11cf0-099e-4e4d-9d64-c12f41e6141d" />


<img width="633" height="431" alt="image" src="https://github.com/user-attachments/assets/e172932b-9925-4783-831f-db85ae44972d" />


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
|   1200:12               |                          |
|   1201:34               |  1204:01                 |              
|   1202:12               |  1205:00                 |
|   1203:34               |  1206:00                 |

#### Manual Calculations

(Add your calculation here)


---<img width="738" height="576" alt="image" src="https://github.com/user-attachments/assets/024d6a5c-9956-4ccd-8751-494f3c7ea6dc" />
## OUTPUT FROM MASM SOFTWARE

<img width="632" height="402" alt="image" src="https://github.com/user-attachments/assets/ac6f1295-504d-4963-9c25-20ffb550aeb7" />

<img width="633" height="428" alt="image" src="https://github.com/user-attachments/assets/a843411d-c272-4138-b7fd-e6633d0d0fc4" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
