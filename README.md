**EXP4:FULL ADDER AND SUBTRACTOR**

NAME: AANANDHA KANNAN.S

REF NO: 24900501

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

1)FULL ADDER

![image](https://github.com/user-attachments/assets/629e4007-3291-4137-8480-b7943814e172)


2)FULL SUBRACTOR

![image](https://github.com/user-attachments/assets/1279277a-080d-49e2-8cfb-b40585fd44f5)



**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:

**1)FULL ADDER **

module fulladder(

input a,b,c,

output sum,carry);

wire w1,w2,w3;

assign sum=a^b^c;
assign w1=a&b;

assign w2=b&c;

assign w3=c&a;

assign carry=w1|w2|w3;

endmodule


**2)FULL SUBRACTOR**

module fullsub(a,b,c,diff,borr);

input a,b,c;

output diff,borr;

wire w1,w2,w3,w4,w5,w6;

xor g1(diff,a,b,c);

and g2(w4,w1,b);

and g3(w5,w1,b);

nd g4(w6,b,c);

or g5(borr,w4,w5,w6);

endmodule


**RTL Schematic**

**1)FULL ADDER **


![Screenshot 2024-12-02 090435](https://github.com/user-attachments/assets/edec3830-0681-420c-9fde-845e6f9ad4a1)


**2)FULL SUBRACTOR **

![Screenshot 2024-12-02 091523](https://github.com/user-attachments/assets/c7f34506-067d-42a6-ada5-039d840c2e7e)



**Output Timing Waveform**

**1)FULL ADDER**

![Screenshot 2024-12-02 090928](https://github.com/user-attachments/assets/fc4c44dd-8657-4197-879b-eeab2e0d098c)



**2)FULL SUBRACTOR**

![Screenshot 2024-12-02 092011](https://github.com/user-attachments/assets/5dc87847-e12f-4d08-8be5-e05175e6c574)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



