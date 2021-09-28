# MilliQan:201 - PMT Dark Current Measurement

Author: Caleb Fangmeier

Last Edited: September 28, 2021

## Abstract

This SOP covers the procedure for measuring the noise of PMTs.

## Required Materials

  - 1x Wrapped PMT to be tested
  - 2x 5V power supplies
  - 1x DRS4 Evaluation Board
  - Misc cables


## Required Training

Users must complete a short training program with either Caleb or another trained person to conduct this activity.

## Procedure

### Connecting the PMT


  1. First, ensure that the 5V supplies (PS 1, and PS 2), and the HV Supply are disabled. For the 5V supplies, they can either be powered off or have their output disabled via pressing the "Output" button until the light turns off. The HV Supply can either be powered off or have its output disabled by switching the toggle labeled "High Voltage" to "STBY/RESET".
  2. Plug in the SHV cable to the large coaxial plug, the SMA cable to the output labeled `OUT A` and the ribbon cable to the matching header as shown below ![]().
  3. Carefully place the assembly laying down inside the dark box. Close the lid.

<img src="https://user-images.githubusercontent.com/2569566/135171865-2d14126b-da74-4f03-a60b-f868b611ea69.png" width="400px">
<img src="https://user-images.githubusercontent.com/2569566/135174236-4a968931-3ac7-469f-9e49-7e0b33d49a7e.jpg" width="400px">


### Powering up the system
![PXL_20210928_195956336](https://user-images.githubusercontent.com/2569566/135174308-ae85a26f-3327-4b2a-a24e-4e6dc872343e.jpg)

  1. If the 5V supplies are off, turn them on with the black toggle-switches on the bottom of their front panels.
  2. Enable the output of PS 1, wait for a couple seconds and then enable PS 2. Check that they both read 5V +- 2mV. If they don't, turn them off and use the top dial to adjust them to 5V.
  3. If the HV suppply is off, turn it on by first ensuring that the toggle-switch labeled "HIGH VOLTAGE" is switched to "STBY/RESET" and then switch the toggle labeled "POWER" to on.
  4. Wait ~15s for the white light indicating "STBY/RESET" to turn on. Then use the dials to select your chosen voltage (by default, we run at -1450V). Ensure that the rightmost dial is set to negative polarity.
  5. Turn on the HV by switching the toggle-switch labeled "HIGH VOLTAGE" to ON.


### Taking data

  1. Start by opening the "DRS Oscilloscope" Application.
  2. The application should startup with the correct settings, but if things have changed, go through the following sequence.
     1. Select the channel you want to collect data on. Normaly, this is channel 1. Set it's vertial scale to 200mV
     2. Set the horizontal scale to 100 ns/Div
     3.  Configure the trigger to `OR` channel 1 only, `AND` no channels, and set the channel 1 (or whatever channel you are using) to a trigger level of 0.020 V.
     4.  Set the trigger mode to "Normal" and polarity to positive.
     5.  Under "Display", enable "Display Date/Time", "Show Grid", and "Show hardware scalers".
  3. To begin aquiring data, make sure at least 3-4 minutes have passed since first turning on the HV. This ensures that the PMT has fully charged and warmed up.
  4. Next, click the "Save" button and save the file using the following convention. `Desktop/MilliQanPMTCal/PMT_SERIAL/YYYY_MM_DD-BIAS_VOLTAGE-SIGNAL_SRC.dat`. Note that you should select "Binary file (\*.dat)" as the file type. Otherwise, substitute the followinig values into the above format.
     - `PMT_SERIAL`: Serial number of PMT (TODO: How to find this)
     - `YYYY`, `MM`, `DD`: today's date. Please add leading zeros when needed. eg. September 26th, 2021 would be `2021_09_26`.
     - `BIAS_VOLTAGE`: Bias voltage for this run
     - `SIGNAL_SRC`: the source of any signal present in the run. If there is no scintillator attached to the PMT, use `nosig`.
  5. Specify the number of events to capture. 10,000 is normally a suitable value.


### Shutting down the system

Shutting down the system is simply a matter of turning off the power supplies.

  1. Turn off the HV supply by first disabling the output using the "HIGH VOLTAGE" toggle and then turning it off with the "POWER" toggle.
  2. The 5V supplies can be turned off by first disabling the output and then switching the power switch at the bottom of the front panel. They will emit a beeping sound for ~5-10s before turning off - this is normal.
