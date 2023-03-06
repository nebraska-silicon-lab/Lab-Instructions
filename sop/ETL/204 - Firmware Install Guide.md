# ETL:204 - Firmware Install Guide
Author: Ian Reed
Last Edited: March 06, 2023

## Abstract
   This SOP covers step-by-step the procedure of installing the firmware to the KCU board

# Start

To upload firmwar to the KCU105, first add this command to your .bashrc
```
get_firmware_zip() {
    version=$1
    project="etl_test_fw"
    projectid="107856"
    file=$project-$version.zip
    url=$(curl  "https://gitlab.cern.ch/api/v4/projects/${projectid}/releases/$version" | jq '.description' | sed -n "s|.*\[$project.zip\](\(.*\)).*|\1|p")
    wget $url
    unzip $file
}
```
To activate either close and reopen the terminal, or run ```source .bashrc``` from your home directory.

You may need to install ```curl``` and ```jq``` for the script to work.
Run the scrip with the version of firmware you want to use

```get_firmware_zip v2.1.2```

Move to the directory that has been created, something like ```etl_test_fw-v2.1.2```
With the board connected and powered on, running ```source program.sh``` will load the firmware to the board. The self test LEDs should now either start "breathing" or "cyloning" to indicate the firmware is loaded.