# Lab 1 - GHDL and GTKWave

## Half Adder Example
```console
ghdl -a ha.vhdl
ghdl -a ha_tb.vhdl
ghdl -e ha_tb
ghdl -r ha_tb --vcd=ha.vcd
gtkwave ha.vcd
```
![Screenshot 2025-05-08 155632](https://github.com/user-attachments/assets/c3e426d8-0e2c-4dfb-b73d-da69997090b8)

![Screenshot 2025-05-08 155613](https://github.com/user-attachments/assets/56014945-65a3-477f-9097-e26cde2f896e)

## 4-to-1 Multiplexer Example
```console
ghdl -a mux.vhdl
ghdl -a mux_tb.vhdl
ghdl -e mux_tb
ghdl -r mux_tb --vcd=mux.vcd
gtkwave mux.vcd
```
![image](https://github.com/user-attachments/assets/a712e2cd-35ff-4911-9601-d6e3c76bfc30)

![image](https://github.com/user-attachments/assets/d5c6ea6e-2676-4d0b-8b82-175d5393ac69)
