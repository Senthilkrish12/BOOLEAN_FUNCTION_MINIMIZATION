### NAME : Senthil Raj G

### REG NO : 212224100054

### EXPERIMENT 2 : IMPLEMENTATION OF BOOLEAN_FUNCTION_MINIMIZATION**


**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**PROCEDURE**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**PROGRAM:**
```
module exp2(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire x1,x2,x3,x4,x5,x6,x7,x8,x9,x10;
assign x1= (~a) & (~b) & (c) & (~d);
assign x2= (a) & (~c) & (~d);
assign x3= (~b) & (c) & (~d);
assign x4= (~a) & (b) & (c) & (d);
assign x5= (b) & (c) & (d);
assign f1= x1|x2|x3|x4|x5;
assign x6= (x) & (~y) & (z);
assign x7= (~x) & (~y) & (z);
assign x8= (~w) & (x) & (y);
assign x9= (w) & (~x) & (y);
assign x10= (w) & (x) & (y);
assign f2= x6|x7|x8|x9|x10;
endmodule
```

**TRUTH TABLE**


![WhatsApp Image 2024-11-21 at 11 34 59_158c6d9f](https://github.com/user-attachments/assets/180440d0-631d-45bf-a85a-4508c9f41e65)

![WhatsApp Image 2024-11-21 at 11 34 59_05329a2a](https://github.com/user-attachments/assets/e7443311-e06d-405a-9194-a60e492f0585)


**RTL REALIZATION**

![WhatsApp Image 2024-11-21 at 10 39 01_59a4773c](https://github.com/user-attachments/assets/d2fe1b17-ec84-43fa-b3be-3e47c39543f7)


**TIMING DIAGRAM**
![WhatsApp Image 2024-11-21 at 10 38 35_6f76205c](https://github.com/user-attachments/assets/77517132-8223-49b6-bad0-8941a4c7875a)

**RESULT**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.
