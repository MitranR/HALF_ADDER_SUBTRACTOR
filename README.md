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

![half-subtractor2](https://github.com/user-attachments/assets/abcf7af3-3f4d-410a-80e4-13daaf168e07)


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
```
Half Adder:
module halfadder(a, b, s, ca);
 input a;
 input b;
 output s;
 output ca;
assign#2 s=a^b;
assign#2 ca=a&b;
endmodule

Half Subtractor:
module halfsub(a, b, dif, bor);
 input a;
 input b;
 output dif;
 output bor;
reg dif,bor;
reg abar;
always@(a or b) begin
abar=~a;
dif=a^b;
bor=b&abar;
end
endmodule

```
/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: Mitran R

RegisterNumber:24006381

**RTL Schematic**
Half Adder:
![3 1 1](https://github.com/user-attachments/assets/eb2cbe81-ae59-43ce-9d58-03d88b4d3eea)

Half Subtractor:
![3 2 1](https://github.com/user-attachments/assets/51da0db6-2cb2-4b1e-a9ff-72e236ff336f)



**Output/TIMING Waveform**

Half Adder:
![3 1 2](https://github.com/user-attachments/assets/088678d8-0d69-4044-9781-194fa735d32f)

Half Subtractor:
![3 2 2](https://github.com/user-attachments/assets/fc1da038-6ac8-4241-b922-f6d95666d08c)


**Result:**
THUS THE BASIC LOGIC GATES ARE STUDIED AND THE TRUTH TABLES ARE VERIFIED
