# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

1.Connect the supply (+5V) to the circuit

2.Switch ON the main switch

3.If the output is 1, then the led glows.

### Program:
```c++
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: MITHUN MS
RegisterNumber: 212222240067
/*
/*Half Adder Program:*/

module HalfAdder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule

/*Full Adder Program:*/

module FullAdder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum=((a^b)^c);
assign carry=((a&b)|(b&c)|(c&a));
endmodule
```
### Output:
### RTL realization:
#### Half Adder:
![Screenshot_20230413_082536](https://user-images.githubusercontent.com/121117266/231637772-100861e7-c480-4d15-85d5-bca6e641810b.png)

#### Full Adder:

![Screenshot_20230413_082555](https://user-images.githubusercontent.com/121117266/231637843-d26f0767-5a24-4c4a-8702-c09abf4f7d17.png)


### TIMING DIAGRAM:

#### Half Adder:
![Screenshot_20230413_082613](https://user-images.githubusercontent.com/121117266/231638028-7d14012f-1188-48e1-81fb-0236e12212e7.png)

#### Full Adder:
![Screenshot_20230413_082630](https://user-images.githubusercontent.com/121117266/231638223-57156274-e6a1-4979-acb4-6d5c786b01ce.png)


### TRUTH TABLE:

#### HAlf Adder:
![Screenshot_20230413_082642](https://user-images.githubusercontent.com/121117266/231638507-30fb6cbe-b9a7-48c0-9eb0-c27b946fe9b6.png)

#### Full Adder:
![Screenshot_20230413_082650](https://user-images.githubusercontent.com/121117266/231638645-b2bdd630-3c54-4129-84ed-3c8c2e00b4ff.png)

### Result:
Thus the half adder and full adder are studied and the truth table for different logic gates are verified.
