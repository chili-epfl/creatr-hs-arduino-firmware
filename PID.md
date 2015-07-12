PID Settings
============

The PID was hand calibrated with intensive love and care. It is meant to run inside the +/- 30C margin and not the
default +/- 10C margin. It is also meant to run with proper D updating when outside the PID zone, which the original
firmware lacks. Just use the firmware in this repo. The values are as follows:

```
P: 11.0
I: 0.2
D: 190.0
```

To set these values, run:

```
M301 P11.0 I0.2 D190.0
M500
```

