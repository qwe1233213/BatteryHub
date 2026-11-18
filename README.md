# BatteryHub (beta)

A tiny Windows tray app that shows the battery level of your wireless devices in one place.

- Lowest battery level right on the tray icon
- One click for the full list of devices
- Low battery warning at 20%
- Optional start with Windows
- About 40 KB, no installer, no account
- Makes no network connections

## Download

1. Open [Releases](../../releases) and download `BatteryHub.zip`.
2. Unzip it and run `BatteryHub.exe`.
3. Look for the round icon near the clock. It may be hidden under the `^` arrow.

The app is not code-signed yet, so Windows SmartScreen may warn you. To run it anyway, choose **More info**, then **Run anyway**. Only do this if you downloaded it from this page.

To quit, right-click the icon and choose **Exit**.

## What has been tested

This is an early beta, tested by one person on one PC (Windows 11, build 26200).

| Method | Devices | Status |
|---|---|---|
| Windows Bluetooth battery value | Bluetooth headsets | Confirmed on Logitech G435 |
| Standard BLE Battery Service | Bluetooth LE mice, keyboards and others | Not confirmed yet |
| Standard HID battery value | Devices that expose it | Not confirmed yet |
| Logitech HID++ | Logitech wireless mice and keyboards | Not confirmed yet |
| Razer | Razer wireless devices | Not confirmed yet |
| AJAZZ 2.4G receiver | AJAZZ AJ139 V2 | Reads a live value, accuracy not confirmed |

Devices that do not report their battery show a dash. Known example: AJAZZ AJ139 V2 over Bluetooth.

Some devices only report in coarse steps, such as 10%.

## Help test it

If you have a wireless device, your report is the most useful thing you can send:

1. Connect the device and run BatteryHub.
2. Right-click the tray icon and choose **Copy test report**.
3. Open a [device report](../../issues/new?template=device-report.yml) and paste it.
4. Add the battery level shown by the device or its official app.

The report contains your Windows build, device names, battery levels and USB/HID model codes. It leaves out Bluetooth addresses and serial numbers, and it tries to remove personal names from device names. Please read it before posting, because a name written in an unusual format may remain.
