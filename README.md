# fmx-gui
Additional controll interface for FMX module in Sunvox

## Problem
Alexander Zolotov is developing an amazing music software studio [Sunvox](https://warmplace.ru/soft/sunvox/). With the version 2 FMX module was introduced. This is a very powerful FM-synth. Due the design concept of Sunvox every controller of a single module is treated equally. On a very complex synth like FMX this concept leads to difficult usage.

## Solution
To be able to work more efficient with the FMX module a special developed external GUI can be used. This GUI is connected via MIDI to Sunvox

## Preparation
1. To use FMX-gui download [Sunvox > v2](https://warmplace.ru/soft/sunvox/), [Open Stage Control](https://openstagecontrol.ammd.net/) and files from this repository.
2. In Sunvox preferences/MIDI enable Midi Through Port-0. Any MIDI-Channel must be accepted. On Linux and Mac this MIDI-Port exists system wide. On windows additional software may be required to create a virtual MIDI-Port.
3. After starting up Open Stage Control add 
``` osc:0,0 ```
in the field "midi".

## Usage
Press play button in Open Stage Control. In the new window Menu/Session/Open -> choose fmx-gui.json from this repository, you downloaded before on your computer.
In Sunvox load the wsch fmx init.sunsynth from this repository, you downloaded before on your computer. Everything is pre-mapped, you ready to go.
The controls of fmx-gui can be moved with the scroll wheel of your mouse, even if Sunvox is active window. This is helpful since virtual keyboard works only, if Sunvox is focused window.
Double click on a controller in fmx-gui resets the value to default.
If you want delete all the MIDI-mappings from FMX-module in Sunvox (for example, if the next patch should be used), you can wrap FMX in a metamodule.
