# DSD

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
# Lexical Elements
- Identifiers
- Keywords
- White Space
- Comments
  
# Data Types
There are four types of data types:  0  1  Z(High Impedencce)  X(Dont Cares)

There are two types of main groups of data types:

* NET: It is the Data type in net group represents the physical connection between hardware components. When a collection of signals is grouped into a bus, we can represent it using a onedimensional array (vector), as in ```wire [N:0] data```
eg:
- wire : The wire data type represents a 1-bit signal
- wand : It is used for wired-and connection
- supply0 : It is used for circuit ground connection
- signed :


* VARIABLE: It is the Data type in variable group represents the abstract storage in behavioral model
eg: (reg, integer, real, time and realtime)
**The most commonly used data type in this group is ```reg``` and it can be synthesized.**

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
### yo

```v

```

## Comments
