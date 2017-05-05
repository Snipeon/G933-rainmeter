# G933-rainmeter

## TUTORIAL STILL INCOMPLETE, PLEASE BEAR WITH ME.

This is a skin to monitor the battery level of your Logitech device through Logitech Gaming Software, however, you would have to use Cheat Engine to pull the base address and pointer offsets of the battery value. Refer to the tutorial below.

Many thanks to Wyse for his G930 rainmeter skin. I took his skin and modified it so that it can work with LGS. 

Wyse: https://github.com/Wyse-/G930BatteryReader

**Downloads:**

Cheat Engine http://www.cheatengine.org/

**Supported devices:**
1. G933 Artemis Spectrum (Currently the only confirmed supported device as I only have this. Anyone who wants to test/modify the program with their device, feel free to do so)

**How to use:**
1. Download and unzip LGSbatt.rar to your rainmeter folder.
2. Download Cheat Engine (Your antivirus may detect it as a virus, don't worry, Cheat Engine is not a virus)
3. Make sure you have LGS running.
4. Install and run Cheat Engine.
5. Grab the required information of your device battery value off Cheat Engine. For the specific device, please consult the device guide below.
6. Run Offsets.exe and key in the information you got off Cheat Engine.
7. Add autostart in the G933 folder to your startup programs list.
8. Load the skin on rainmeter.
9. Restart your computer and enjoy!

**Device Guide:**
- G933 Artemis Spectrum
  - For the G933, the battery value is stored on LGS as an integer value from 0 to 100. Basically, what percent battery you see, it is stored exactly as that value. Here's how to grab the addres for that value with Cheat Engine.
  1. When you run Cheat Engine, you would see a window like this.
  2. Click on the Select process to open button.
  3. Select LCore.exe from the list.
  4. Under the value, key in your battery value and click first scan. (You may wanna have LGS open so you can track the battery value)
  5. From here on, it's time to play the waiting game. Wait for your battery value to drop, careful not to let the G933 go into sleep. Keep updating the value and clicking next scan in Cheat Engine to reflect your current battery value. You should end up with about 6 values in the end. (I only have 3 values cuz I cheated. I didn't have LGS open.)
  6. Close the LGS window and reopen it. Do not close the process, just close it to the taskbar. you should see 3 of the values start to change while the other 3 stays unchanged. The unchanged values are the ones you want. Double click on the 3 values and you should see them be added to the list.
  7. Now we need to do a pointer scan of all 3 values. Right click on the first value and select pointer scan for this address. A window like this should come out click ok and save the file as something you can keep track of. Then let the scan run and you should end up with something like this. Now do the same for the other values.
  8. Ok, here's the hardest part. Turn off your G933 and turn it back on. Then redo steps 4 to 6 to grab 3 new addresses to narrow down the pointer scan.
  9. 
