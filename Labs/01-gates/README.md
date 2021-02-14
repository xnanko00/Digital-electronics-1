# 1. cvičenie

## GitHub link

https://github.com/xnanko00/Digital-electronics-1

# 2. cvičenie

## De Morganove zakony

### vzorec

![Vzorce](/Labs/01-gates/Images/vzorec1.gif)

### VHDL kód
```VHDL
architecture dataflow of gates is
begin
	f_o <= ((not b_i) and a_i) or ((not c_i) and (not b_i));
    fnand_o <= not (not ((not b_i) and a_i) and (not((not c_i) and (not b_i))));
    fnor_o <= not (b_i or (not a_i)) or (not (c_i or b_i));

end architecture dataflow;
```
### Screenshot

![Screenshot](/Labs/01-gates/Images/scr1.png)

### EDA Playground link

https://www.edaplayground.com/x/E2GK

### Tabuľka

| **c** | **b** |**a** | **f(c,b,a)** |
| :-: | :-: | :-: | :-: |
| 0 | 0 | 0 | 1 |
| 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 0 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 0 | 0 |
| 1 | 0 | 1 | 1 |
| 1 | 1 | 0 | 0 |
| 1 | 1 | 1 | 0 |
<!--- 
# 3. cvičenie

## Boolova algebra

### vzorec

![Vzorce](/Labs/01-gates/Images/vzorec2.gif)

### VHDL kód
```VHDL
architecture dataflow of gates is
begin
	f0_o <= x_i and not(x_i);
    f1_o <= (x_i or not(x_i));
    f2_o <= (x_i or  x_i or  x_i);
    f3_o <= (x_i and x_i and x_i);

end architecture dataflow;
```

### Screenshot

![Screenshot](/Labs/01-gates/Images/scr2.png)

### EDA Playground link

https://www.edaplayground.com/x/dGbB

### Tabuľka

|**x** | **x and not x** | **x or not x** | **x or x or x** | **x and x and x** |
| :-: | :-: |  :-: | :-: |  :-: |
| 0 | 0 | 1 | 0 | 0 |
| 1 | 0 | 1 | 1 | 1 |

--->
# 3. cvičenie 

## Distributive laws 

### vzorec

![Vzorce](/Labs/01-gates/Images/vzorec3.gif)

### VHDL kód
```VHDL
architecture dataflow of gates is
begin
    f10_o <= (x_i and y_i) or (x_i and z_i);
    f11_o <= (x_i and (y_i or z_i));
    f20_o <= (x_i or y_i) and (x_i or z_i);
    f21_o <= x_i or (y_i and z_i);

end architecture dataflow;
```

### Screenshot

![Screenshot](/Labs/01-gates/Images/scr3.png)

### EDA Playground link

https://www.edaplayground.com/x/8Nqu

### Tabuľka


| **z** | **y** |**x** | **x and y or x and z** | **x and (y or z)** | **(x or y) and (x or z)**  | **x or (y and z)**  |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 0 | 0 | 0 | 0 |
| 0 | 1 | 1 | 1 | 1 | 1 | 1 |
| 1 | 0 | 0 | 0 | 0 | 0 | 0 |
| 1 | 0 | 1 | 1 | 1 | 1 | 1 |
| 1 | 1 | 0 | 0 | 0 | 1 | 1 |
| 1 | 1 | 1 | 1 | 1 | 1 | 1 |