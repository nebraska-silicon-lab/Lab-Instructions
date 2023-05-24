# ETL:201 - Vivado Install Guide
Author: Ian Reed
Last Edited: May 24, 2023

## Abstract
   This SOP covers step-by-step the procedure of installing the Vivado software on an Ubuntu 20.04 LTS machine. RHEL based systems should also work.

# Start
Use the Batch Mode Installation Flow, outlined in this pdf starting on page 47:

https://docs.xilinx.com/v/u/2019.2-English/ug973-vivado-release-notes-install-license

This is a terminal based, which is more reliable than the GUI version.

You will likely need to install this package
```sudo apt install libtinfo5```
otherwise the installation will not complete, hanging on the finishing stage.

Navigate here:
https://www.xilinx.com/support/download/index.html/content/xilinx/en/downloadNav/vivado-design-tools/2021-1.html

We want the 2021.1 version of the package. Of the 3 options, select

```Xilinx Unified Installer 2021.1 SFD (TAR)```

a tar file that contains the programs we want to use. The file is rather large and can take some time to download depending on network speeds. Unpack it with the command:

```tar -xvf Xilinx_Unified_2021.1_0610_2318.tar.gz```


With the file unpacked, navigate to the new directory. First, make a install config file with
```./xsetup -b ConfigGen```
and follow the prompts on the terminal to create the file. Select Vivado(option 2) if you want to be able to edit code, or Lab Edition (option 5) if you just want to upload firmware. In the case of a Vivado installation, you will need a software key from the lab manager. Make sure to select the Enterprise version of Vivado, otherwise you will not be able to program the board.

The script will tell you the location of the newly created config file. You can open the file to make changes, but the defaults should be fine. With the config file ready, use this command to begin the install process
```./xsetup --agree XilinxEULA,3rdPartyEULA,WebTalkTerms --batch Install --config <path/to/config>```
Installation shouldn't take too long, O(30min). This process may be repeated if different Vivado versions need to be installed, just rerun the config creation command with different options to get the relevant config files.

For the following script to work, make sure to add the path to Vivado to you $PATH. You can do so by adding 
```export PATH="/tools/Xilinx/Vivado/2021.1/bin/:$PATH"```
to your .bashrc file. You can get the specific path from the desktop icon created when installing Vivado
