# DSD

# Table of Contents
- **Unit 1**
  + [Lexical Elements](#lexical-elements)
  + [Data Types](#data-types)
  + [Magnitude Comparators](#magnitude-comparators)
  + 
  
# Lexical Elements
- Identifiers
- Keywords
- White Space
- Comments
  
# Data Types
There are four types of data types: 
- 0
- 1
- Z (High Impedencce)
- X(Dont Cares)

There are two types of main **groups** of data types:

* NET: It is the Data type in net group represents the physical connection between hardware components. When a collection of signals is grouped into a bus, we can represent it using a onedimensional array (vector), as in ```wire [N:0] data```
eg:
  - wire : The wire data type represents a 1-bit signal
  - wand : It is used for wired-and connection
  - supply0 : It is used for circuit ground connection
  - signed :
  

* VARIABLE: It is the Data type in variable group represents the abstract storage in behavioral model
eg: (reg, integer, real, time and realtime)

**The most commonly used data type in this group is ```reg``` and it can be synthesized.**

# Magnitude Comparators

## 1bit Comparator

```v
module eq1
(input wire i0,i1,
output wire y);
Wire p0,p1;
Assign y=p0|p1;
Assign p0=i0&i1;
Assign p1=~i0&~i1;
endmodule
```

## 2-bit magnitude comparator

```v
module mag_comp(
    input wire [1:0] a,b
    output wire eq
);
wire p0,p1,p2,p3;

    assign eq = p0|p1|p2|p3;
    assign p0 = (~a[1];
    assign B_greater = (A < B);

endmodule

```

## STRUCTURAL DESCRIPTION 
- A digital system is frequently composed of several smaller subsystems.
- This allows us to build a large system from simpler or predesigned components.
- Verilog provides a mechanism, known as module instantiation, to perform this task.
- This type of code is called Structural Description.
  
```v
module eq2
(
input wire [1:0] a, b,
output wire q
};

// internal signal declaration
wire eO, el;
// bodv
// instantiate two 1-bit comparators

eql eq-bit0-unit (.iO(a [O] ) , .il (b LO]) , .eq(e0)) ;
eql eq-bitl-unit (.eq(el), .iO(a[ll), .il(bC11)) ;
15 // a and b are eqrral if individual bits are equal
assign aeqb = eO & el;
endmodule 
```

## Verilog Primitive

Verilog primitive Verilog includes a set of predefined primitives that can be instantiated FYI as modules. These primitives correspond to simple gate-level function blocks, such as the and, or, and not cells.

![Screenshot from 2023-09-13 09-02-53](https://github.com/akshatva7/DSD/assets/135726741/124214dd-c67f-4dcc-acff-14d78d99135a)

This form of code is very tedious and can easily be replaced with simple bitwise logical  operators. In addition to the predefined primitives, we can also define customized primitives, known
as user-defined primitives (UDPs).

## Testbench
After code is developed, it can be simulated in a host computer to verify the correctness of the circuit operation and can be synthesized to a physical device. Simulation is usually performed within the same HDL framework.

## Operators

![Screenshot from 2023-09-13 09-21-02](https://github.com/akshatva7/DSD/assets/135726741/f696d8e4-d0bb-4ae8-afce-066ac64a2c72)


### Precedence

![Screenshot from 2023-09-13 09-16-47](https://github.com/akshatva7/DSD/assets/135726741/03e53314-7960-4521-a35d-cf161958bb1a)

### Relational Operators

![Screenshot from 2023-09-13 09-39-29](https://github.com/akshatva7/DSD/assets/135726741/cd2aa07a-3903-480e-a122-74162a33cc69)

### Bitwise and Logical Operators
![Screenshot from 2023-09-13 09-41-24](https://github.com/akshatva7/DSD/assets/135726741/5142932f-a529-4ef6-87f1-a53e89e4c6c8)







