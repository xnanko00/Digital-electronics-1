# 1. cvičenie

## GitHub link

https://github.com/xnanko00/Digital-electronics-1

# 2. cvičenie

## De Morganove zakony

### vzorec

![Vzorce](/Labs/01-gates/Images/vzorec1.gif)

### VHDL kód
```
architecture dataflow of gates is
begin
    f_o  <= ((not b_i) and b_i) or ((not c_i) and (not b_i));
    fnand_o <= (not(a_i) or not(b_i) or not(c_i));
    fnor_o <= (not(a_i) and not(b_i) and not(c_i));

end architecture dataflow;
```
### Screenshot

![Screenshot](/Labs/01-gates/Images/scr1.png)

### EDA Playground link

https://www.edaplayground.com/x/E2GK

### Tabulka
| **c** | **b** |**a** | **f(c,b,a)** | **f(c,b,a)nand** | **f(c,b,a)nor** |
| :-: | :-: | :-: | :-: | :-: | :-: |
| 0 | 0 | 0 | 1 | 1 | 1 |
| 0 | 0 | 1 | 1 | 1 | 0 |
| 0 | 1 | 0 | 0 | 1 | 0 |
| 0 | 1 | 1 | 0 | 1 | 0 |
| 1 | 0 | 0 | 0 | 1 | 0 |
| 1 | 0 | 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 0 | 1 | 0 |
| 1 | 1 | 1 | 0 | 0 | 0 |