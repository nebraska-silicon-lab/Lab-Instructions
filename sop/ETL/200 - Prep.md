# ETL:200 - Prep
Author: Ian Reed
Last Edited: May 24, 2023

## Abstract
   This SOP covers the procedure of installing some needed software on an Ubuntu 20.04 LTS machine. RHEL based systems should also work.

# Start
While this step is not needed to install Vivado, if these are not in the system, the module test software won't work.
It is better to do them now, as OS refershes/changes were needed to diagnose this problem and avoiding having to download Vivado several times is in your best interest.

First, update the system and install git and python

```
sudo apt update
sudo apt upgrade
sudo apt install git
sudo apt install python3.8
```

THe update step might do the python3.8, but this is fine.

Next, install the packages needed to compile the ipbus software

```sudo apt-get install -y make erlang g++ libboost-all-dev libpugixml-dev python-all-dev rsyslog```

with the needed packages ready, download, compile, and install ipbus
```
git clone --depth=1 -b v2.8.3 --recurse-submodules https://github.com/ipbus/ipbus-software.git
cd ipbus-software
sudo make PYTHON=python3
sudo make install PYTHON=python3
```
With this finished, check that the install worked. Use the first command to temporarily set the ipbus path, then open a session of python and import uhal
```
export LD_LIBRARY_PATH=/opt/cactus/lib:$LD_LIBRARY_PATH
python3
import uhal
```
If there are no errors while importing, everthing worked and you can continue the installation process.
