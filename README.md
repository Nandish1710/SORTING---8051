
# SORTING---8051

**AIM:**

To write and execute Assembly language Program for sorting of data using 8051 keil.

**APPARATUS REQUIRED: Personal computer with Keil software**

**(i) Descending order ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is low, then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H 

MOV R6,#04

LOOP: MOV A,@R0 

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT 

SJMP DOWN 

NEXT:JNC DOWN 

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END


**OUTPUT:**

**MEMORY WINDOW:**

Before execution: D:0x40H:

<img width="936" height="274" alt="508690962-98f3cd45-9a9b-4e27-84ce-565fe1e9fdc2" src="https://github.com/user-attachments/assets/e67ca6f5-8333-41c7-90cc-b74448870955" />

After execution: D:0x40H:

<img width="985" height="304" alt="508691089-4911b41d-7e3e-4916-a641-51210e8702c2" src="https://github.com/user-attachments/assets/6a839b04-01ce-48be-9408-5851ec4802c9" />


**(ii)	Ascending order**
 
**ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is high then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H

MOV R6,#04

LOOP: MOV A,@R0

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT

SJMP DOWN 

NEXT:JC DOWN

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END

**OUTPUT:**

**MEMORY WINDOW:** 

**Before execution:**
D:0x40H:

<img width="950" height="272" alt="508691155-7355b788-4bbf-4295-8223-e33d4676eb6e" src="https://github.com/user-attachments/assets/9731ccd1-3b20-4ebb-9f4d-758f800bec64" />

After execution:
D:0x40H:

<img width="984" height="291" alt="508691193-bd54a79d-9563-4de9-85ec-8ccae73462d6" src="https://github.com/user-attachments/assets/3aa084ba-8eda-4a4d-8806-32d0d02e4eb0" />

**Result:**

Thus the sorting of given data was done using 8051 keil and shown the output.

