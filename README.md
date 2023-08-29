# DSD

## 1bit Comparator

```
module eq1
(input wire i0,i1,
output wire y);
Wire p0,p1;
Assign y=p0|p1;
Assign p0=i0&i1;
Assign p1=~i0&~i1;
endmodule
```

# Data Types
There are four types of data types:  0  1  Z(High Impedencce)  X(Dont Cares)

There are two types of main groups of data types:

* NET: It is the Data type in net group represents the physical connection between
hardware components - (wire, wand, signed, supply0)
* VARIABLE: It is the Data type in variable group represents the abstract storage in
behavioral model - (reg, integer, real, time and realtime)

## 2-bit magnitude comparator

```
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
## Comments
