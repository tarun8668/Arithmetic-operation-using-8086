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

<img width="639" height="398" alt="Screenshot 2025-08-30 092240" src="https://github.com/user-attachments/assets/225f1df6-69bb-46e6-b780-13f857cb5475" />

<img width="658" height="413" alt="Screenshot 2025-08-30 092600" src="https://github.com/user-attachments/assets/62c14c68-8ab6-477d-99fc-06c7a297eddf" />

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

<img width="651" height="385" alt="Screenshot 2025-08-30 093222" src="https://github.com/user-attachments/assets/c70762a8-40e7-4c56-8eb6-53031e6c5be5" />

<img width="635" height="410" alt="Screenshot 2025-08-30 093121" src="https://github.com/user-attachments/assets/d86e6ae2-92a5-4bf4-8459-b6a8e2cdf225" />



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

 <img width="552" height="328" alt="Screenshot 2025-08-30 093434" src="https://github.com/user-attachments/assets/785b5129-1bf6-4b6c-a461-ef885a697f9c" />

 <img width="660" height="411" alt="Screenshot 2025-08-30 093647" src="https://github.com/user-attachments/assets/4c691dfa-a0ac-4df4-90ba-c68c4620f470" />


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

<img width="635" height="338" alt="Screenshot 2025-08-30 093945" src="https://github.com/user-attachments/assets/9db0ac03-8acd-4d11-af7f-b0e01fe43c3f" />

<img width="655" height="411" alt="Screenshot 2025-08-30 094212" src="https://github.com/user-attachments/assets/e620def0-02e9-463d-872f-ced8e1d532cf" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
