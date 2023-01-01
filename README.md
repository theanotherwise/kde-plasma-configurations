```bash
konsole --tabs-from-file konsole.tabs --profile  TheAnotherWise
```

```bash
qdbus org.kde.plasmashell /PlasmaShell evaluateScript "lockCorona(true)"

qdbus org.kde.plasmashell /PlasmaShell evaluateScript "lockCorona(false)"
```

`/etc/X11/xorg.conf`

```bash
Section "Device"
    Identifier      "intel"
    Driver          "intel"
    BusId           "PCI:0:2:0"
    Option          "TearFree"      "true"
    Option          "DRI"           "3"
EndSection

Section "Screen"
    Identifier      "intel"
    Device          "intel"
EndSection
```
