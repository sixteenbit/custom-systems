# RetroPie 4.4 for Sixteenbit Systems

Scripts for setting up RetroPie on a Gameboy Zero.

## What's in the box

1. Optimized [config.txt](settings/config.txt) which includes overclocking
1. Download Gameboy Zero splashscreen by [AJRedfern](https://www.sudomod.com/forum/viewtopic.php?f=8&t=1440)
1. Install the gbz35 theme and set it as default
1. Install the gbz35-dark
1. Enable 30sec autosave on roms
1. Disable 'wait for network' on boot

## Flashing the pre-configured image

A preconfigured image is available to flash at https://github.com/sixteenbit/retropie-i2s/releases. Download the latest release and flash the .img to an SD card (e.g. using [Etcher](https://etcher.io/) or [Apple Pi Baker](https://www.tweaking4all.com/software/macosx-software/macosx-apple-pi-baker/))

## Running the installer

1. Download RetroPie from the [official site](https://retropie.org.uk/download/)
1. Flash the .img to an SD card (e.g. using [Etcher](https://etcher.io/) or [Apple Pi Baker](https://www.tweaking4all.com/software/macosx-software/macosx-apple-pi-baker/))
1. Enable WIFI and SSH
1. `git clone https://github.com/sixteenbit/retropie-i2s.git`
1. `cd retropie-i2s`
1. `sudo ./install.sh YES`
1. `sudo reboot now`

## Post installation

### Update all the things

```bash
sudo apt-get update; sudo apt-get upgrade -y;
```

### Install Retrogame

```bash
cd; curl https://raw.githubusercontent.com/adafruit/Raspberry-Pi-Installer-Scripts/master/retrogame.sh >retrogame.sh
sudo bash retrogame.sh
```

### Install i2s Script

```bash
curl -sS https://raw.githubusercontent.com/adafruit/Raspberry-Pi-Installer-Scripts/master/i2samp.sh | bash
```

### Install Battery Monitor

This is a [modified version](https://github.com/sixteenbit/Mintybatterymonitor) of HoolyHoo's [Mintybatterymonitor](https://github.com/HoolyHoo/Mintybatterymonitor).

1. `wget https://raw.githubusercontent.com/sixteenbit/Mintybatterymonitor/master/MintyInstall.sh`
1. `sudo git clone https://github.com/sixteenbit/Mintybatterymonitor.git`
1. `sudo chmod 777 MintyInstall.sh`
1. `sudo ./MintyInstall.sh`
1. `sudo reboot now`


## Credits

- Installer script originally built by [Kite](https://github.com/kiteretro/Circuit-Sword) for the Circuit Sword but has been re-purposed for Gameboy Zero.
- MintyBatteryMonitor is a modified version of [HoolyHoo's](https://github.com/HoolyHoo/Mintybatterymonitor).
- Splashscreen was created by [AJRedfern](https://www.sudomod.com/forum/viewtopic.php?f=8&t=1440)
