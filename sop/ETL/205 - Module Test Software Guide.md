# ETL:205 - Module Test Software Guide
Author: Ian Reed
Last Edited: March 06, 2023

## Abstract
   This SOP covers step-by-step the procedure of installing the module test software to the PC connected to the KCU board
   
# Start
This guided is a modified version of this guided
https://etl-rb.docs.cern.ch/Software/module-test/
Please check here for more details

To use the module test software,  several dependencies are needed.

If using a RHEL based version of linux, install 'ipbus for uhal' with
```sudo yum install cactuscore-uhal-python3```
If on a Debian/Ubuntu based version of linux, you can attempt to compile from source following these instructions:
https://ipbus.web.cern.ch/doc/user/html/software/install/compile.html
I encountered issues with this method and chose to use the docker container preped by BU. This can be downloaded and installed with the command:
```docker run -it --name tamalero danbarto/centos-uhal-py3:latest /bin/bash```
which will pull the latest version of the container, then start it up. All work with the test software must be done inside the container. 

While insided the container, clone the git repo with the module test software
```git clone https://gitlab.cern.ch/cms-etl-electronics/module_test_sw.git```

Further instrucions on running the software can be found at the github on the software
