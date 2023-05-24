# ETL:203 - BOard Communication Setup
Author: Ian Reed
Last Edited: May 24, 2023

## Abstract
   This SOP covers step-by-step the procedure of installing the necessary drivers and selecting the proper setting to comunicate the the KCU board
   
# Start
First, install the Vivado cable drivers

```
cd ${vivado_install_dir}/data/xicom/cable_drivers/lin64/install_script/install_drivers/
./install_drivers
```
Next, set the  clock for the board. Use
```screen /dev/ttyUSB0 115200```
to make the connecting. If the menu does not show, press space
From the menu select ```1. Set Programmable Clocks```
followed by ```1. Set KCU105 Si570 User Clock Frequency```
with a value of ```320.64MHz```
Save (3)->(1)->(0)

Check the clock value with ```5. View KCU105 Saved Clocks in EEPROM```

We want these setting to survive power cycling the board, so go to ```6. Set KCU105 Clock Restore Options```
Select option (2)
Return to Clock Menu (0)

To exit the screen session, ```crtl-k```

Next, configure the ethernet to be able to communicate with the board. This is needed for the module test software.
Open your network settings, naviate to the IPv4 tab of the ethernet port connected to the KCU, switch to 'Manual'
Set the address to ```192.168.0.XXX``` and Netmask to ```255.255.0.0```
XXX can be any value not already taken on the network. For simple setups with only the KCU and no other hardware ```20``` is a good default value
