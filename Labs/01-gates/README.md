#1. cvičenie
##GitHub link

#2. cvičenie
## De Morganove zakony

###vzorec
\begin{align*}
    f(c,b,a) =&~ \overline{b}\,a + \overline{c}\,\overline{b}\\
    f(c,b,a)_{\textup{NAND}} =&~ \overline{abc}\ =&~ \overline{a}+\overline{b}+\overline{c}\\
    f(c,b,a)_{\textup{NOR}} =&~ \overline{a+b+c}\ =&~ \overline{a}\,\overline{b}\,\overline{c}\\
\end{align*}

###VHDL kód
```
architecture dataflow of gates is
begin
    f_o  <= ((not b_i) and b_i) or ((not c_i) and (not b_i));
    fnand_o <= (not(a_i) or not(b_i) or not(c_i));
    fnor_o <= (not(a_i) and not(b_i) and not(c_i));

end architecture dataflow;
```
###Screenshot

###EDA Playground link

###Tabulka
| **c** | **b** |**a** | **f(c,b,a)** | **f(c,b,a)** | **f(c,b,a)** |
| :-: | :-: | :-: | :-: | :-: | :-: |
| 0 | 0 | 0 | 1 | 1 | 1 |
| 0 | 0 | 1 | 1 | 1 | 0 |
| 0 | 1 | 0 | 0 | 1 | 0 |
| 0 | 1 | 1 | 0 | 1 | 0 |
| 1 | 0 | 0 | 0 | 1 | 0 |
| 1 | 0 | 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 0 | 1 | 0 |
| 1 | 1 | 1 | 0 | 0 | 0 |