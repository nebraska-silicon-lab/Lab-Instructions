# ETL:203 - BOard Communication Setup
Author: Ian Reed
Last Edited: March 06, 2023

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
Use NetworkManager with a command like this

```nmcli connection add type ethernet ifname enp0s31f6 con-name kcu105 ip4 192.168.0.130/24 gw4 192.168.0.255```

ifname = the hardware name of the ethernet port, can be found with ```nmcli device```
con-name = name of the connection you are making. I used kcu105 for simplicity
ip4 = ip address and subnet setting to talk the the board
gw4 = broadcast to talk to the board

I would like to provide more explanation for the ip4 and gw4, but I don't fully understand their meaning. I know this worked for me.
To test if you can talk to the board run ```ping 192.168.0.10```, or whatever you have set the board ip to be.
