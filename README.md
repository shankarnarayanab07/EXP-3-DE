# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**
**HALF-ADDER**

<img width="583" height="337" alt="Half-adder" src="https://github.com/user-attachments/assets/c4f64940-37d9-478d-8025-e739e55c883c" />

**HALF-SUBTRACTOR**

<img width="601" height="337" alt="Half-subtractor " src="https://github.com/user-attachments/assets/71131329-6d9a-4047-a8c1-036e17294f4d" />


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: Shankar Narayana B RegisterNumber: 25009078*/
**Half-Adder**
```
module half_adder(sum, carry, a, b);
  output sum;
  output carry;
  input a;
  input b;
  assign sum = a ^ b;
  assign carry = a & b;
endmodule

```
**Half-Subtractor**
```
module half_subtractor(diff, borrow, a, b);
  output diff;
  output borrow;
  input a;
  input b;
  assign diff = a ^ b;
  assign borrow = ~a & b;
endmodule

```

**RTL Schematic**
**Half-Adder**
<img width="1920" height="1200" alt="HA-1" src="https://github.com/user-attachments/assets/d746dc68-e74d-45c4-973e-de49faab82dc" />
**Half-Subtractor**
<img width="1920" height="1200" alt="HS-1" src="https://github.com/user-attachments/assets/b928e9fd-2d4e-46d7-8f14-1beb4276d8dc" />


**Output/TIMING Waveform**
**Half-Adder**
<img width="1920" height="1200" alt="HA-2" src="https://github.com/user-attachments/assets/f04d03e9-bb91-4152-839a-49a4e3d57a38" />
**Half-Subtractor**
<img width="1920" height="1200" alt="HS-2" src="https://github.com/user-attachments/assets/dfd72c26-ab8d-421d-8ecd-9bcdcef95c50" />

**Result:**
Thus the Half Adder and Half Subtractor are studied and the truth tables are verified
