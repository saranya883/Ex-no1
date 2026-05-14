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
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table


 <img width="510" height="377" alt="image" src="https://github.com/user-attachments/assets/d403e48a-879d-47b2-b416-7cb3041ee686" />


#### Manual Calculations


 <img width="332" height="212" alt="image" src="https://github.com/user-attachments/assets/32cacd5b-3858-4d01-9aba-72dad9b05a5f" />

 
---

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="551" height="377" alt="image" src="https://github.com/user-attachments/assets/0b258847-7329-45ab-ad75-5880261d05ec" />

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

 <img width="466" height="253" alt="image" src="https://github.com/user-attachments/assets/7e5f2f80-89eb-44b5-8683-4c1edb50fdce" />


#### Manual Calculations


 <img width="397" height="198" alt="image" src="https://github.com/user-attachments/assets/fc806dfb-40f4-4feb-bd6b-427ba438dbd7" />


---


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="551" height="387" alt="image" src="https://github.com/user-attachments/assets/14a9948b-5686-44a5-8f15-1843b726bd49" />

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


 <img width="457" height="251" alt="image" src="https://github.com/user-attachments/assets/1afd90dd-2fbe-4cd3-bc74-725b7a18417c" />


#### Manual Calculations


 <img width="441" height="223" alt="image" src="https://github.com/user-attachments/assets/c52b2037-3455-4c15-8f4c-6d904040bd5d" />

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="547" height="375" alt="image" src="https://github.com/user-attachments/assets/a8038c55-a6e8-4fa8-8e45-748b6737dd51" />

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

 <img width="472" height="282" alt="image" src="https://github.com/user-attachments/assets/047656e5-efe4-4c86-8966-475ef82101ca" />

#### Manual Calculations


 <img width="358" height="135" alt="image" src="https://github.com/user-attachments/assets/24e53080-723b-4caf-829a-673f08877537" />

## OUTPUT FROM MASM SOFTWARE


<img width="541" height="382" alt="image" src="https://github.com/user-attachments/assets/47986a8f-063f-46b6-a034-56c5156120e1" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

