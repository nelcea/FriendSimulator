# Friend Simulator

Simulator of BasedHardware Friend device.

This is an early version, code needs cleaning, proper error handling, ...

## Limitations

On the Mac, name advertised for the BLE Peripheral is the name of the machine.  
The Friend app looks for a device named "Friend" (or "Super").

One solution is to rename your machine to one of those names.  
Another solution is to rebuild the Friend app yourself.  
In AppWithWearable project, in file /lib/utils/ble/scan.dart, at line 11, add the name of your machine to the condition, like  
``` dart
(device) => device.name == 'Friend' || device.name == 'Super' || device.name == 'my machine name',
```
