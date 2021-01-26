# mywinhere

Script to move all windows to main monitor

Switching on and off mutiple monitors result in windows being spread all over.

Using this script to move all windows to primary monitor.

### Motivation

Using multiple monitors. On linux I use a script that issue *xrandr* commands to switch around active monitors. E.g.

```sh
mymon 3 # Use 3 monitors
mymon r # Only right-hand monitors
mymon c # Only center monitor
```
.. etc.

Isue is when switching, the open windows are moved (randomly) around all monitors. I have most on primary monitor, and can move the few I need to the other after first moving all to one.

### Example output:

```sh
$ mywinhere -d
DESKTOP: 0 4650x1680
PRIMARY: Left.Top 1050.600   Right.Bottom 2970.1680

Dryrun

ACT   CurX   CurY =>  NewX   NewY  TITLE
      1741    627                  Some window
      1060    635                  Another window
GET:    10     19 =>  1060    619  Another window
      1060    635                  Another window
GET:     0      0 =>  1050    600  user@FOO:~
GET:    42     92 =>  1092    692  user@FOO:~
GET:  2980    638 =>  1060     -1  Another window
GET:  2970    628 =>  1050     -1  Another window
```

**ACT** show *GET* if window is moved. *NewX* and *NewY* are new coordinates. If `-1` it means keep current.

## Sample pictures

### Before

<img src="https://raw.githubusercontent.com/Termplexed/mywinhere/Termplexed-sample-images/before-scaled.jpg" />

### After

<img src="https://raw.githubusercontent.com/Termplexed/mywinhere/Termplexed-sample-images/after-scaled.jpg" />
