# mywinhere

Script to move all windows to main monitor

Switching on and off mutiple monitors result in windows being spread all over.

Using this script to move all windows to primary monitor.

### Example output:

```bash
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
