# The Stress Terminal UI: s-tui

s-tui is a terminal UI add-on for stress. The tool uses stress to run CPU hogs, while monitoring the CPU usage, temperature and frequency of your computer.

This software makes it possible to stress and monitor your computer without a need for a GUI. 

### Pros
* Monitoring your headless server over ssh
* See performance dips caused by thermal throttling 
* Requires minimal resources


## Simple Installation:
* Download and unzip the directory or clone from github
```
git clone https://github.com/amanusk/s-tui.git
```
* install stress (See dependencies)
```
sudo apt-get install stress
```
* run `(sudo) ./s-tui`

## Screen Shots
![](./ScreenShots/stui1.png?raw=true "Full Screen")

![](./ScreenShots/stui2.png?raw=true "Overheat detected")

![](./ScreenShots/stui3.png?raw=true "Two Graphs")


## Dependencies
s-tui uses stress. To install stress on Ubuntu run:
```
sudo apt-get install stress
```

## Usage
To run the compiled executable simply run:
```
(sudo) ./s-tui
```

## To run .py file
If would like to make changes to s-tui, you can test your work by running s-tui.py.

s-tui uses psutil and urwid libraries.
These need to be installed to run s-tui.py
```
(sudo) pip install urwid
(sudo) pip install psutil
```
then run 
```
(sudo) ./s-tui.py
```

## Compatibility
s-tui uses psutil to probe your hardware information. If your hardware is not supported, you might not see all the information.

Running s-tui as root gives access to the maximum Turbo Boost frequency available to your CPU when stressing all cores. (Currently tested on Intel only).

Running without root will display the Turbo Boost available on a single core. 


