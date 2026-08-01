<p align="center">
  <a href="https://9buildhk.com">
    <img src="./assets/9build-mark.svg" alt="玖造 9 Build" width="68">
  </a>
</p>

<h1 align="center">香港鐵路到站屏 / HK Railway ETA Display</h1>

<p align="center"><strong>Community Edition</strong></p>

<p align="center">
  <a href="README.md">English</a> ·
  <a href="README.zh-HK.md">繁體中文（香港）</a>
</p>

<p align="center">
  <a href="https://github.com/9build/hk-railway-eta-display-ce/releases">
    <img src="https://img.shields.io/github/v/release/9build/hk-railway-eta-display-ce?display_name=tag&amp;sort=semver&amp;label=latest%20release" alt="Latest release">
  </a>
  <a href="https://github.com/9build/hk-railway-eta-display-ce/releases">
    <img src="https://img.shields.io/github/downloads/9build/hk-railway-eta-display-ce/total?label=downloads" alt="GitHub release downloads">
  </a>
</p>

<p align="center">
  <a href="https://9buildhk.com">9buildhk.com</a> ·
  <a href="../../releases">GitHub Releases</a> ·
  <a href="../../releases/latest/download/FLASHING.md">English flashing guide</a> ·
  <a href="../../releases/latest/download/FLASHING.zh-HK.md">繁體中文（香港）刷寫指南</a>
</p>

> A desk display for checking the next MTR Heavy Rail arrivals at a glance.

Join a compatible 2.4 GHz Wi-Fi network directly on the display—no phone app or separate gateway is needed. HK Railway ETA Display then reads public MTR ETA data and shows the next trains, platforms, and destinations. It is made by [玖造 9 Build](https://9buildhk.com) in Hong Kong.

## Highlights

<table>
  <tr>
    <td width="33.33%" align="center" valign="top">
      <img src="./assets/ce-live-eta.png" alt="Live ETA in the 9 Build device frame" width="100%"><br>
      <strong>Live ETA</strong><br>
      <sub>See the next arrivals, platforms, and destinations.</sub>
    </td>
    <td width="33.33%" align="center" valign="top">
      <img src="./assets/ce-line-picker.png" alt="MTR line picker in the 9 Build device frame" width="100%"><br>
      <strong>Choose a line</strong><br>
      <sub>Select the line and station you want to follow.</sub>
    </td>
    <td width="33.33%" align="center" valign="top">
      <img src="./assets/ce-baked-ad.png" alt="Built-in information and advertising display in the 9 Build device frame" width="100%"><br>
      <strong>Built-in display</strong><br>
      <sub>ETA screens can alternate with a built-in information or advertising display.</sub>
    </td>
  </tr>
</table>

Product features and screen designs may improve in future releases. Always check the release notes before installing a new version.

## Install Community Edition

Use the installer for a classic ESP32-WROOM-32E board with an **ILI9341V** display. Download the matching file and `SHA256SUMS` from [GitHub Releases](../../releases), then verify the checksum:

```sh
shasum -a 256 platform9-ce-esp32e-ili9341-28-install.bin
```

Flash the merged installer with Espressif `esptool`. Replace the serial port with your own:

```sh
python3 -m esptool --chip esp32 --port /dev/cu.usbserial-XXXX --baud 460800 erase-flash
python3 -m esptool --chip esp32 --port /dev/cu.usbserial-XXXX --baud 460800 write-flash --flash-size 4MB 0x0 platform9-ce-esp32e-ili9341-28-install.bin
```

For Windows commands, USB download mode, and troubleshooting, read the [English flashing guide](../../releases/latest/download/FLASHING.md) or [繁體中文（香港）刷寫指南](../../releases/latest/download/FLASHING.zh-HK.md). Arduino IDE is not the supported installer path.

## Before downloading

Read the release `LICENSE.txt`. Community Edition may be installed and used only on hardware you own and directly control for personal, private, non-commercial use. The licence included with each release is the controlling version.

## Links

- [玖造 9 Build · 9buildhk.com](https://9buildhk.com)
- [Download page](https://9buildhk.com/#download)
- [Community Edition Releases](../../releases)
- [MTR Open Data ETA endpoint](https://rt.data.gov.hk/v1/transport/mtr/getSchedule.php)

This is an independent, unofficial product. It is not affiliated with or endorsed by MTR Corporation, DATA.GOV.HK, or any railway operator.
