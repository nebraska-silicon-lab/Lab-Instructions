# ETL:106 - Wirebond Encapsulation

Author: **Jahid Hossain**, Caleb Fangmeier

Last Edited: February 14, 2023

## Abstract
   This SOP covers step-by-step the procedure of encapsulating the wire bonds on assembled modules.


## Required Tools and Materials

  ### Instruments for the Encapsulation
  
   - Nordson EFD 3-Axis EV Series Automated Fluid Dispensing Robot
   - Nordson EFD's Ultimus I dispensers
   - Height Sensor 
   - Fully assembled module on carrier
 <table>
  <tr>
    <td><img src="https://github.com/jhosain/Lab-Instructions/blob/5c053aab6d16644239808934567de8e67dd6179b/sop/ETL/106_materials/images/Mini_Gantry.png" alt="Alt Text" height="500"></td>
    <td><img src="https://github.com/jhosain/Lab-Instructions/blob/49ff5233f0ebae66c431dc95049ced5a41a420ab/sop/ETL/106_materials/images/Height_Sensor.png" alt="Alt Text" height="500"></td>
  </tr>
</table>
  
  ### Tools and Materials to Prepare the Encapsulant
  
   - Centrifugal Machine
   - Sylgard 186 Silicon Elastomer Kit (Base & Curing Agent)
   - Nordson EFD 2K 50ml Manual Cartidges Dispenser Gun, 10:1 ratio
   - Nordson EFD 2-Part Cartidegs with Sealing Cap, 10:1 ratio
   - Nordson EFD 2K, 10:1 S & L 50ML Pistons
   - Nordson EFD Precison Tips: 23GA (Orrange) 30GA (Pink) 32GA (Yellow)
   - Electronic Balance
   - Disposable Spiral Mixer and 1cc & 10cc Syringe, and Spatula
   - Optimum Syringe Barrel (5cc), Syringe Barrel Adapters, Piston and Tip Caps 
   - Vacuum Oven

<table>
  <tr>
    <td><img src="https://github.com/jhosain/Lab-Instructions/blob/adc72fadc96f47e0cd351dcefd4421fe60658971/sop/ETL/106_materials/images/Mixing_tools.pmg.png" alt="Alt Text" height="500"></td>
  </tr>
</table>

## Required Software

Nordoson Dispense Motion
Windows based Operating System


## Required Training

Users must complete a short training program with either Caleb or another trained person to conduct this activity.

## Procedure

### Encapsulant (Sylgard 186) Mixing Procedure

 - Place the 2-Part Cartidge barrale on a stand to hold (wear the gloves). 
 - Using a 1cc syring fill up the thin part of the 2 part cartidge by the sylgard curing agent and seal it up by the piston
 - Using a 10cc syringe or using an spatula fill up the thicker part of the 2 part cartidge and seal it up by the piston
 - Setup the cartidge barrel in the dispenser gun                                                                                                           
 
 

### Encapsulation Procedure

  ### Step 1: Preapring and Moungint the Dispenser Syringe 
  
  - Plug the static spiral mixer to the cartidge barrel 
  - Fill up the 5cc syringe barrel (Needle side is closed by the tip cap) by pressing the gun 
  - Use the centrifuge machine to remove the air bubbles from the dispensing syrige barrel
  - Replace tip cap with a precision dispanse tip from the syringe barrel and attach it to the adapter assembly
  - Mount the syringe on the robot
  
  ### Step 2: Purging the Dispenser Syring 
  
  ### Step 3: Starting the Program
  
  ### Step 4: Calibrating the Needle Tip 
  
  - Hit the "Needle Z Detect" button to calibrate the z height. 
  - Hit the "Needle XY Adjust" button to calibrate the X & Y position. 
  
  ### Step 5: Despensing (Potting)
  
  ### Step 6: Removing Syring from Holder
  
  ### Step 7: Saving and Ending the Program
  
  ### Step 8: Creating and Publishing Report
  
  ### Step 9: Transfering Plates to the Curing Vacuum Oven
  
  ### Step 10: Transfering Modules to the Carrier
  
  ## Results 
  

  - Needle tip size
  - Air Pressure
  - Encapsulant Bead Dimensions (Width, lenght, Height)
  - Tip and Bond Pad Gap
  - Rate of motion of the Syringe ( Flow Rate)
  - Number of Passes
  - Line Dispense Setup
  - Backtrack Setup
  - Z Clearance Setup
  - Timming
  - Curing Time
  - Bead Dimension after Curing
  - Bead Dimension on PCB w/wo wirebonds
  - Bead Dimension on Glass Plate
  - Bead Dimension vs Speed/Air_Pressure/Tip_Gap/Pass_No/Time/Cure_Time/Tip_Size/Surface


  ## Timming
   
  - Mixing sylgard and filling cartidg barrel: ~ 30 mins
  - Mixing, filling syringe, degassing (removing air bubbles), mounting syringe on robot: ~ 10 mins
  - Calibration and pruging time: ~ 10 mins
  - Potting Time 
  * 1 pass ~ 3.5 mins and Total time for a single module ~ 15 mins
  * 2 passes ~ 7 mins on a pad. Total time for four pads ~ 30 mins
  
  - Useful Pot life from time of mix ~ 90 mins
  
  - Curing time at room temperuture ~ 8 hrs
  - Curing time in oven at 60˚C ~ 30 mins and at 50˚C ~ ?
  

  ## Height Sensor Mounting and Programming
  
  ## Example Scripts
  
  ## Dispenser Manuals and Documentations
