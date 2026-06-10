### Pre-installation:

* **HyperOS latest stable based on Android 15 firmware is required As of now Global HOS OS OS3.0.6.0.WNPMIXM **
* Optional gapps (from download page, gapps button)

### First time installation (clean flash):

* Extract the following images from the ROM package:
  * boot.img
  * dtbo.img
  * init_boot.img
  * vendor_boot.img

* Power off the device and boot into Fastboot mode:
  * Hold **Volume Down + Power** until **FASTBOOT** appears on the screen.

* Flash the required images:

```bash
fastboot flash boot boot.img
fastboot flash dtbo dtbo.img
fastboot flash init_boot init_boot.img
fastboot flash vendor_boot vendor_boot.img
```

* Boot directly into recovery.
* Navigate to Apply Update > Apply from ADB
* Sideload the ROM:

```bash
adb sideload crDroid-*-peridot.zip
```

* Factory reset / Format data
* Reboot to system
* If you want to use your own Google Apps package, NikGApps is recommended. Reboot back into recovery after ROM installation and sideload the GApps package.

### Update installation:

#### Via recovery (recommended way):

* Boot to recovery
* Choose Apply Update and Apply from ADB
* Install crDroid zip via sideload and reboot

```bash
adb sideload crDroid.zip
```

* If you had GApps, reboot to recovery and sideload gapps.zip, then reboot

#### Via OTA:

* Go to Settings -> System -> Updater and download latest build
* Choose install and let it finish
* Reboot
