# snes-northsec-2021
Source code for the Super Nintendo Reverse Engineering Challenges From NorthSec CTF 2021.

These challenges required you to provide the correct input in order to calcualte the correct offsets used to print the flag.

For a comprehensive writeup, please read the very neat work done by Ben Gardiner (@0xstatic):
https://gist.github.com/BenGardiner/13fe76fd43f179a872acbb9f5729eb2c

Another writeup is available thanks to the Hubert Hacking CTF team:
https://huberthackin.gitlab.io/posts/nsec21-rare-metal-sequencer/
https://huberthackin.gitlab.io/posts/nsec21-rare-metal-sequencer-2/

## LEVEL 1 solution
Requires you to understand what are the expected inputs on Joypad-01.

check_1 
- Button_Y

check_2
- Button_B + Button_Down

check_3
-  Button_Select + Button_Up

check_4
- Button_L



FLAG-PBR9YUHHQYRMC9QR7TQQQKBGMC



## LEVEL 2 solution
Requires you to understand what are the expected inputs on both Joypad-01 and Joypad-02.

check-1 
- player two input
- Button_Y Joy-2


check-2 
- XOR with 0x71
- joy_1=Button_B (0x80 xor 0x71 = 0xF1)


check-3
- joy-1 + joy-2 input combined
- joy_2=Button_L joy_1=Button_A


check-4
- ROR input 1
- joy_1=Button_Y (0x40 --ROR--> 0x20)


FLAG-QYR88WNDGBWXRGW4XRGW49GE5W

