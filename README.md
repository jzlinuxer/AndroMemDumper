# AndroMemDumper
AndroMemDumper is a tool used to dump the memory of a specific process on Android.

##Dependency
python2.7 

##Platform
Tested on Ubuntu12.04_64 and window7_64

##Usage
Run the following command<br>
```Bash
python dump.py -pid <PID> -saddr <start_addr> -eaddr <end_addr>
```
* <PID>: a specific process's pid
* <start_addr>: start address of dumped memory
* <end_addr>: end address of dumped memory
* The address of dumped memory's last byte is actually <end_addr>-1
* The size of dumped memory is <end_addr>-<start_addr>
* The dumped memory will be saved to current work directory
Example<br>
```Bash
python dump.py -pid 1317 -saddr b43ed000 -eaddr b43ef000
```
* Running the cmd above will dump the memory between [b43ed000,b43ef000).

##Note
* The bin/dumpMemory tool works for Android 5.1.1 (32bit-arm) emulator and didn't test on other android versions or real devices.
