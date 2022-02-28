# LD19 Lidar udev Rule

This directory contains a udev file that is used to create a Symlink device named `/dev/ldlidar` when the CP2102 USB to UART Bridge Controller
is used with the LD19 Lidar.

## Usage

Copy the included udev rules file to your host's udev rules. Then retrigger the new rule.

```
cp 99-ldlidar-usb-uart.rules /etc/udev/rules.d/99-ldlidar-usb-uart.rules
```

Now we need to retrigger this new dev rule.

```
sudo udevadm trigger
```

Once the CP2102 USB UART is detected we should see a symlinked device at `/dev/ldlidar`

## How this file was created

