# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by:NITHISH S

RegisterNumber: 212224240105
```
module NITHISH(a,b,c,d,w,x,y,z,f1,f2);
  input a,b,c,d,w,x,y,z;
  output f1,f2;
  wire x1,x2,x3,x4,x5,y1,y2,y3,y4,y5;
  assign x1=((~a)&(~b)&(~c)&(~d));
  assign x2=(a&(~c)&(~d));
  assign x3=((~b)&(c)&(~d));
  assign x4=((~a)&(b)&(c)&(d));
  assign x5=(b&(~c)&(d));
  assign f1=x1|x2|x3|x4|x5;
  
  assign y1=(x&(~y)&(z));
  assign y2=((~x)&(~y)&z);
  assign y3=((~w)&x&y);
  assign y4=(w&(~x)&(y));
  assign y5=(w&x&y);
  assign f2=y1|y2|y3|y4|y5;
  endmodule
*/
```

**TRUTH TABLE**
![WhatsApp Image 2025-04-16 at 09 01 00_ef757f19](https://github.com/user-attachments/assets/83b7ec9e-fd57-446a-9b8b-cc9f2423400a)
![WhatsApp Image 2025-04-16 at 09 01 12_4d9526b8](https://github.com/user-attachments/assets/918a7bd6-1ce8-4b33-b145-d068dedf7b7e)

**RTL**
![Screenshot 2025-04-16 084326](https://github.com/user-attachments/assets/1eeda609-5d84-47d9-91cd-5957b2a9d051)

**WAVEFORM**
![WhatsApp Image 2025-04-16 at 09 11 13_9c8b72e8](https://github.com/user-attachments/assets/f3cb4657-c234-4515-b8c7-fcca8ae5358e)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

