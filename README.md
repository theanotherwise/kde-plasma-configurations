```bash
konsole --tabs-from-file konsole.tabs --profile  TheAnotherWise
```

## KDE Plasma Widgets

```bash
qdbus org.kde.plasmashell /PlasmaShell evaluateScript "lockCorona(true)"

qdbus org.kde.plasmashell /PlasmaShell evaluateScript "lockCorona(false)"
```

## Intel as Display, NVIDIA for Cuda

### Select

```bash
prime-select on-demand
```

### Force Xorg to use Intel

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

`/etc/modprobe.d/i915.conf`

```bash
options i915 enable_psr=0
```
