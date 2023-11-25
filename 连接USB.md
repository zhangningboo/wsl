### 将usb设备连接到wsl

```shell
PS C:\Users\ningd> usbipd wsl list
BUSID  VID:PID    DEVICE                                                        STATE
...      ...       ...                                                          Not attached
3-1    2bc5:0511  USB Camera                                                    Not attached
4-2    2bc5:0614  ORBBEC Depth Sensor                                           Not attached

PS C:\Users\ningd> wsl --list
适用于 Linux 的 Windows 子系统分发:
docker-desktop-data (默认)
docker-desktop
Ubuntu-22.04
Ubuntu-18.04
PS C:\Users\ningd> usbipd wsl attach -d Ubuntu-18.04 --busid 3-1

PS C:\Users\ningd> usbipd wsl list
BUSID  VID:PID    DEVICE                                                        STATE
...      ...       ...                                                          Not attached
3-1    2bc5:0511  USB Camera                                                    Attached - WSL
4-2    2bc5:0614  ORBBEC Depth Sensor                                           Not attached
```