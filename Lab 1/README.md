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


