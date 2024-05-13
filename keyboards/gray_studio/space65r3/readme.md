# Gray Studio Space65 R3

A 65% keyboard by Graystudio. PCB designed and manufactured by DEMO Studio.

* Keyboard Maintainer: [edwardslau](https://github.com/edwardslau)
* Hardware Supported: Space65 R3
* Hardware Availability: [Graystudio.club](https://graystudio.club/products/gb-space60-%E2%85%B2)

Make example for this keyboard (after setting up your build environment):

    make gray_studio space65r3:default

Flashing example for this keyboard:

    make gray_studio space65r3:default:flash

## Bootloader
* **Physical reset button**: Briefly press the button on the back of the PCB - some may have pads you must short instead

See the [build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) and the [make instructions](https://docs.qmk.fm/#/getting_started_make_guide) for more information. Brand new to QMK? Start with our [Complete Newbs Guide](https://docs.qmk.fm/#/newbs).


# For V custom keymap and enable via

```shell
make gray_studio/space65r3:v
```

```shell
make gray_studio/space65r3:v:flash
```

# 刷机报错，但是不影响刷机

```shell
➜  qmk_firmware git:(bd60) ✗ make gray_studio/space65r3:v:flash
Making gray_studio/space65r3 with keymap v and target flash

arm-none-eabi-gcc (Arm GNU Toolchain 13.2.rel1 (Build arm-13.7)) 13.2.1 20231009
Copyright (C) 2023 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

Size before:
   text    data     bss     dec     hex filename
      0   37014       0   37014    9096 gray_studio_space65r3_v.bin

Compiling: quantum/via.c                                                                            [OK]
Linking: .build/gray_studio_space65r3_v.elf                                                         [OK]
Creating binary load file for flashing: .build/gray_studio_space65r3_v.bin                          [OK]
Creating load file for flashing: .build/gray_studio_space65r3_v.hex                                 [OK]

Size after:
   text    data     bss     dec     hex filename
      0   37014       0   37014    9096 gray_studio_space65r3_v.bin

Copying gray_studio_space65r3_v.bin to qmk_firmware folder                                          [OK]
Flashing for bootloader: stm32duino
dfu-util 0.11

Copyright 2005-2009 Weston Schmidt, Harald Welte and OpenMoko Inc.
Copyright 2010-2021 Tormod Volden and Stefan Schmidt
This program is Free Software and has ABSOLUTELY NO WARRANTY
Please report bugs to http://sourceforge.net/p/dfu-util/tickets/

Opening DFU capable USB device...
Device ID 1eaf:0003
Device DFU version 0110
Claiming USB DFU Interface...
Setting Alternate Interface #2 ...
Determining device status...
DFU state(2) = dfuIDLE, status(0) = No error condition is present
DFU mode device DFU version 0110
Device returned transfer size 2048
Copying data from PC to DFU device
Download        [=========================] 100%        37016 bytes
Download done.
DFU state(8) = dfuMANIFEST-WAIT-RESET, status(0) = No error condition is present
Resetting USB to switch back to runtime mode
Done!
make[1]: *** [flash] Error 74
make: *** [gray_studio/space65r3:v:flash] Error 1
Make finished with errors

```


```commandline
qmk flash -kb gray_studio/space65r3 -km v
```
