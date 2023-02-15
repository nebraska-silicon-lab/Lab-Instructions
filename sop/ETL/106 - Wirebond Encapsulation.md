# ETL:106 - Wirebond Encapsulation

Author: **Jahid Hossain**, Caleb Fangmeier

Last Edited: February 14, 2023

## Abstract
   This SOP covers the procedure for the encapsulation.
   
## Required Materials

  ### Instruments for the Encapsulation
  
   - Nordson EFD 3-Axis EV Series Automated Fluid Dispensing Robot
   - Nordson EFD's Ultimus I dispensers
   - Height Sensor 
   - Optimum Syringe Barrel (5cc), Syringe Barrel Adapters, Piston and Tip Caps 
   - Nordson EFD Precison Tips: 23GA (Orrange) 30GA (Pink) 32GA (Yellow)
   - Centrifuge Machine
  
  ### Materials to Prepare the Encapsulant
  
   - Sylgard 186 Silicon Elastomer Kit (Base & Curing Agent)
   - Nordson EFD 2K 50ml Manual Cartidges Dispenser Gun, 10:1 ratio
   - Nordson EFD 2-Part Cartidegs with Sealing Cap, 10:1 ratio
   - Nordson EFD 2K, 10:1 S & L 50ML Pistons
   - Disposable Spiral Mixer and 1cc, 5cc & 10cc Syringe, and Spatula

## Required Software

Nordoson Dispense Motion


## Required Training

Users must complete a short training program with either Caleb or another trained person to conduct this activity.

## Procedure

### Encapsulant (Sylgard 186) Mixing Procedure

 - Place the 2-Part Cartidge barrale on a stand to hold (wear the gloves). 
 - Using a 1cc syring fill up the thin part of the 2 part cartidge by the sylgard curing agent and seal it up by the piston
 - Using a 10cc syringe or using an spatula fill up the thicker part of the 2 part cartidge and seal it up by the piston
 - Setup the cartidge barrel in the dispenser gun                                                                                                              <img src="https://github.com/jhosain/Lab-Instructions/blob/patch-1/sop/ETL/106_materials/images/dispenser_gun.jpeg" width="400px">
 
 

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
  
  ### Step 5: Placing the Module Chucks on the Robot
  
  ### Step 7: Setting and Running the Program (Potting)
  
  ### Step 8: Removing Syring from the Holder 
  
  ### Step 9: Saving and Ending the Program
  
  ### Step 10: Creating and Publishing Report
  
  ### Step 11: Transfering Plates to the Curing Vacuum Oven
  
  ### Step 12: Transfering Modules to the Carrier
  
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

  ## Line Dispanse Programming
  
   - Start Program
   - Z clearence
   - Line Dispense Setup  
   - Measuring the Z-Height using Height Sensor
   - Detecting the X, Y & Z cordinates of the Bond Pads and Updating the Program
   - Backtrack Setup
   - Repate the process for other bond pads
   - End Program

  ### Example Scripts
  
  ## Height Sensor Mounting and Programming
  
  ## Dispenser Manuals and Documentations
