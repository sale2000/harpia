# harpia

## Flash the stock ROM or the files


```bash
#!/bin/bash

fastboot oem fb_mode_set
sleep 2
#fastboot flash partition gpt.bin
#fastboot flash logo logo.bin
fastboot flash boot boot.img
sleep 2
fastboot flash recovery recovery.img
sleep 2
fastboot flash system system.img_sparsechunk.0
sleep 2
fastboot flash system system.img_sparsechunk.1
sleep 2
fastboot flash system system.img_sparsechunk.2
sleep 2
fastboot flash system system.img_sparsechunk.3
sleep 2
fastboot flash system system.img_sparsechunk.4
sleep 2
fastboot flash system system.img_sparsechunk.5
sleep 2
fastboot flash oem oem.img
sleep 2
fastboot flash modem NON-HLOS.bin
sleep 2
fastboot erase modemst1
sleep 2
fastboot erase modemst2
sleep 2
fastboot flash fsg fsg.mbn
sleep 2
fastboot erase cache
sleep 2
fastboot erase userdata
sleep 2
fastboot erase customize
sleep 2
fastboot erase clogo
sleep 2
fastboot erase DDR
sleep 2
fastboot oem fb_mode_clear
sleep 2
fastboot reboot
```



