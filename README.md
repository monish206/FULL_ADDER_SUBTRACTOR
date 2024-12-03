# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
![fd908383-0c72-4631-92fa-38e74c3deb30](https://github.com/user-attachments/assets/33678520-3948-454f-b18f-a13e071e8c68)

![505e1ca8-6901-4d20-b652-899a5e4e9b87](https://github.com/user-attachments/assets/e047918d-684c-4c64-97a3-f5aa9eb6854f)


**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
```
module exp4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
wire sl,cl,c2;
xor (sl,a,b);
and (cl,a,b);
xor (sum,sl,cin);
and (c2,sl,cin);
or (cout,c2,cl);
endmodule
```
```
module EXP_4 (df,bo,a,b,bin);
 output df;
 output bo;
 input a;
 input b;
 input bin;
 wire w1,w2,w3;
 assign w1=a^b;
 assign w2=(~a&b);
 assign w3=(~w1&bin);
 assign df=w1^bin;
 assign bo=w2|w3;
 endmodule
```
Developed by:MONISH KUMAR N       
RegisterNumber:24012059


**RTL Schematic**
![exp4](https://github.com/user-attachments/assets/c309ab4a-60c6-409b-8a04-906407f5584a)

![b62dbf77-278c-4c40-88f9-ce067392564c](https://github.com/user-attachments/assets/8a24534a-43b1-4c9e-9b84-840ec9cd44ad)

**Output Timing Waveform**
![c85e65a3-6c5e-428c-831e-e924566eecee](https://github.com/user-attachments/assets/56bb9068-5780-44aa-b7ec-3a041e8365c3)

![899e3478-a7b6-4e36-b7a6-257af5640898](https://github.com/user-attachments/assets/64d20ae8-32cf-4dbe-86a2-05aae2a73ebb)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



