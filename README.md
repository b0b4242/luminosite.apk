# Brightness control for Fire TV Stick

The Fire TV Stick has no built-in brightness setting, so this small free app dims the screen with a semi-transparent black overlay.

> The app's interface is in French, but all you need to know is this:
>
> - **UP arrow** = brighter
> - **DOWN arrow** = darker
> - LEFT / RIGHT also work: right = brighter, left = darker

It goes from 100% down to 20% in steps of 5%. It can't go above your TV's maximum brightness, since it only dims.

## Setup

1. In **Downloader**, enter this link and install:

   `https://github.com/B0b4242/luminosite.apk/releases/download/latest/luminosite.apk`

2. Enable ADB debugging (**Settings > My Fire TV > Developer options**), connect with adb, and run this once:

   `adb shell appops set com.jp.luminosite SYSTEM_ALERT_WINDOW allow`

3. Open the app (it's called **Luminosité** on the home screen) and use the arrows. Your setting is restored after a reboot.

## Notes

- Tested on a Fire TV Stick 4K (Fire OS 6.7.1.1).
- Some streaming apps draw video on a hardware layer that may not be dimmed.
- The app has no internet permission and collects no data.
