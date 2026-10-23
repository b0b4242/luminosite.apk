# Brightness control for Fire TV Stick

The Fire TV Stick has no built-in brightness setting, so this small free app dims the screen with a semi-transparent black overlay.

> The app's interface is in French, but here are the controls:
>
> - **UP / RIGHT** = brighter, **DOWN / LEFT** = darker (1% per press, hold to go faster)
> - **OK** = night mode on/off (warm orange tint)
> - **Menu (≡)** = settings: night mode intensity and sleep timer options
> - **Play/Pause** = start/stop the sleep timer
> - Any other button closes the app (your setting stays active)

Brightness goes from 100% down to 5%. It can't go above your TV's maximum brightness, since it only dims.

## Themes

Seven color themes (classic, ocean, forest, aurora, rose, sunset, pure black) in the settings (Menu > Thème). Night mode always keeps its warm amber look.

## Night mode

Adds a warm tint on top of the dimming. In the settings (Menu) you can choose the warmth (5% to 100%) and the tint: amber, sepia, red or honey.

## Sleep timer

Gradually lowers the screen brightness (and optionally the volume) over time. In the settings you can choose:

- duration (5 min to 3 h) and an optional delay before it starts
- final brightness, and final volume (or leave the volume untouched)
- curve: how the drop is shaped over time (linear, smooth, very smooth, slow start, very slow start, fast start, very fast start, or in steps), with a small preview graph
- turn night mode on when it starts
- at the end: do nothing, or pause playback (the volume goes back to its starting level)

The volume fade only affects the Fire Stick's own audio volume, not your TV's volume. Changing the brightness by hand stops the timer.

## Setup

1. In **Downloader**, enter this link and install:

   `https://github.com/B0b4242/luminosite.apk/releases/download/latest/luminosite.apk`

2. Enable ADB debugging (**Settings > My Fire TV > Developer options**), connect with adb, and run this once:

   `adb shell appops set com.jp.luminosite SYSTEM_ALERT_WINDOW allow`

3. Open the app (it's called **Luminosité** on the home screen) and use the remote. Your setting is restored after a reboot.

## Notes

- Tested on a Fire TV Stick 4K (Fire OS 6.7.1.1).
- Some streaming apps draw video on a hardware layer that may not be dimmed.
- The app has no internet permission and collects no data.
