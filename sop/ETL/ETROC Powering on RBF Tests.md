# ETROC Powering on RBF Tests

Authors: Hayden Swanson and Naomi Gonzalez
Aide: Alex Madorsky

## Abstract
This SOP covers how to test if the ETROC is receiving the correct power during all of its functions, but focuses on investigating further on power characteristics when running noisewidth and baseline tests to understand the "etoc getting stuck" issue. 


## Preperation

### Materials
- oscilliscope + differential probes 
    - Previously used: LeCroy PP007-WR / PP007-WS Passive Probe
- rbf3 v4.7 (with external vref jumpers) + module pcb v4.4
- Teststand - KCU105 + v3.2.4 firmware + Tamalero (on the master branch, commit:`1ab1bdf447fdf242d577c457b1e49d3b329f34c6`)


### Setup 
1. Connect the module to slot 1 on rbf3, LV connector to power supply, and VTRX+ to kcu
    - if using external VREF make sure you have the correct jumpers soldered onto the board!
2. Connect the oscilliscope probe to the rbf (Fig 1)
     - ground -> GND
     - signal -> one of the two testpoint
3. Set up scope settings - DC, bandwidth = 20 MHz, vert. scale: 100 mV per division, horizontal scale: 100..200 uS per division
4. Select trigger channel to be the one were you connected the oscilliscope probe and select Auto trigger mode
5. Check oscilliscope viewing window
    - The scope should show a horizontal line at the 1.2V level (when the module power is on). You may need to move the signal down using vertical position knob so you see that horizontal line.
    - If possible, try increasing the scale to 50 mV per division and moving the signal line down so it's still visible on the screen. If that does not work, stay with 100 mV
8. Adjust the trigger level to 1.1V
    - This is 100 mV below the horizontal line on the screen (when the module power is on).  This is done so the scope will trigger on any dips in the power voltage
9. Switch the trigger into Normal mode
    - Now it will only redraw the signal when the trigger condition happens (aka a dip in voltage)
10. Power cycle power supply and run test_tamalero to check fiber connections
    - Make sure you have module_test_sw installed, and move into that directory
    - `source setup.sh`
    - `python test_tamalero.py --power_up`

At this point the set-up is ready to run tests.

Here are the final suggested settings you should have on your scope:

### Channel Settiings
| Vertical Scale | Offset | Coupling | Bandwidth    |
| -------------- | ------ | -------- | --- |
| 100mV          | -1V    | DC1MOhm  |  20MHz   |
### Timebase
| Timebase | Time/Division | Delay |
| -------- | -------- | -------- |
| RealTime     | 100uS     | 0     |
### Trigger
| Type | Trigger Channel    | Coupling | Trigger Level    | Slope    |
| ---- | ------------------ | -------- | --------- | -------- |
| Edge | One with the probe | DC       |  1.150V   | Positive |

No Holdoff

If your scope has the capabilities, you can also consider setting up your scope to save the waveforms out after every trigger. 
 
## Test Directions
When running the test please make sure to record the flavor and serial number of the RBF, the serial number and version of the module pcb, and the test point which you are monitoring. Repeat the test three times in the bad state AND three times in the good state. In the end, per testpoint, you should have 6 sequence waveform outputs.

0. Place the Probe on the test point of interest with the associated ground like in Figure 2
1. Run test module tamalero
    - `python test_module.py --test_chip --external_vref --moduleid 123` (if external vref otherwise drop the `--external_vref`)
2. Watch for triggers 
3. When the script begins the autothreshold scan, document if it is stuck or not
    - STUCK: calibration is exceeding 7min
    - GOOD: Calibration is less than 7min
4. Once documented, kill the process
5. Repeat steps 1 through 4 until you have atleast 3 good and 3 bad waveforms

If you  run into any other errors like invalid memory when trying to read a node, just retry the script

## Figures
Figure 1:
![](https://codimd.web.cern.ch/uploads/upload_5fc2d8f35b21d9fea262f4c07b1106f7.png)

Figure 2:
![](https://codimd.web.cern.ch/uploads/upload_462cbf78ec0a497541aadce668257788.png)

### Lablogs
- [Unstuck commands](https://bu.nebraskadetectorlab.com/submission/9334)
- [Inital lablog](https://bu.nebraskadetectorlab.com/submission/6398)

