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

<img width="642" height="261" alt="image" src="https://github.com/user-attachments/assets/6b2516a1-b675-4d1b-8a13-dde5f2b413aa" />


#### Manual Calculations

<img width="810" height="580" alt="image" src="https://github.com/user-attachments/assets/2d19e8e0-84d3-4b7e-ba9b-0c3eae8de46d" />

---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="624" height="384" alt="Screenshot 2025-09-06 081913" src="https://github.com/user-attachments/assets/e497e5e4-f3f0-4a81-aca3-ad59fe83ee5b" />
<img width="640" height="395" alt="Screenshot 2025-09-06 081740" src="https://github.com/user-attachments/assets/7353e0cf-f2e2-44d3-b10c-66a0b4d39291" />


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
<img width="651" height="232" alt="image" src="https://github.com/user-attachments/assets/5232cd68-fa35-4acc-ad8c-41c4fb825186" />


#### Manual Calculations

<img width="795" height="801" alt="image" src="https://github.com/user-attachments/assets/01374224-a23e-441a-9f6b-602f5620e667" />


---


## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-06 at 09 12 35_07764360](https://github.com/user-attachments/assets/53028475-41ba-4896-8152-fef6437a77e9)
![WhatsApp Image 2025-09-06 at 09 12 35_94ed1276](https://github.com/user-attachments/assets/9152d0ee-cab3-4cfd-96f0-c3b3ed1eb978)



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
<img width="648" height="260" alt="image" src="https://github.com/user-attachments/assets/43bb5470-83be-4c0a-be46-24789a6ca0d1" />




#### Manual Calculations

<img width="674" height="691" alt="image" src="https://github.com/user-attachments/assets/526d8a2a-b77e-4fb1-8127-8ba17c0fbbf3" />


---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="620" height="374" alt="Screenshot 2025-09-06 091543" src="https://github.com/user-attachments/assets/7e6f312c-2082-4dbb-bb28-1d65ca9c70f6" />
<img width="643" height="404" alt="Screenshot 2025-09-06 091323" src="https://github.com/user-attachments/assets/94a22107-c153-4c2f-859c-096f4b72a99b" />


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

<img width="652" height="247" alt="image" src="https://github.com/user-attachments/assets/852c9a39-7abd-4ee5-b968-913ce3dfd7e1" />


#### Manual Calculations

<img width="517" height="589" alt="image" src="https://github.com/user-attachments/assets/a4bab116-fcd9-404c-9894-9aa29babaf05" />


---
## OUTPUT FROM MASM SOFTWARE
<img width="639" height="390" alt="Screenshot 2025-09-06 092451" src="https://github.com/user-attachments/assets/960f34b3-7d31-4670-9e50-a1712ba5890e" />
<img width="622" height="398" alt="Screenshot 2025-09-06 092350" src="https://github.com/user-attachments/assets/8624236d-0df3-4b43-8448-710fa13aca11" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
