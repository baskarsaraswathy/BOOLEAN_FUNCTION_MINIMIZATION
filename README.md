# EXP 02-BOOLEAN_FUNCTION_MINIMIZATION
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
```

module ex01san(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);

and g1(s,ydash,z);
and g2(t,x,y);
and g3(u,w,z);
or g4(f2,s,t,u);
endmodule


```

Program for logic gates and verify its truth table in quartus using Verilog programming.

# Developed by : BASKAR J 
# RegisterNumber : 212223040025


**RTL realization**

![Screenshot 2024-03-24 204436](https://github.com/baskarsaraswathy/BOOLEAN_FUNCTION_MINIMIZATION/assets/144871005/dee09fd9-6b44-40ef-afbf-d6ab2e627d53)

**Truth Table**

![image](https://github.com/baskarsaraswathy/BOOLEAN_FUNCTION_MINIMIZATION/assets/144871005/96ebeb42-3093-489e-b6ab-688e9a11d038)

 
**Timing Diagram**
![image](https://github.com/baskarsaraswathy/BOOLEAN_FUNCTION_MINIMIZATION/assets/144871005/4e9caee5-196e-49c4-8caf-a081849bc641)


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

