# `mpc-qt-assoc-install.bat` <img src="https://raw.githubusercontent.com/he3als/mpc-qt-assoc-install/mpc-qt-document.png" align="right">

This script is a fork of [mpv-install](https://github.com/rossy/mpv-install), and sets up file associations for [mpc-qt](https://github.com/mpc-qt/mpc-qt) on Windows.

## How to install

1. Make sure you have the latest build of mpc-qt. Official builds are here:
   https://mpc-qt.github.io/downloads.html
2. Download the zip: https://github.com/he3als/mpc-qt-assoc-install/archive/master.zip
3. Run `mpc-qc-assoc-install.bat`. **Note:** For an unattended install, use the `/u` switch. Optionally, a path can be specified, like `/u "%cd%\mpc-qt.exe"`
4. Use *Windows Settings/Default Programs* and *AutoPlay* settings to make mpc-qt the default player

You will be prompted to manually specify your `mpc-qt` executable path if:
- The script is not already ran inside an mpc-qt directory
- If mpc-qt is not installed via [Scoop](https://scoop.sh/)
- If mpc-qt is not in `%PATH%`

## What it does

- Creates file associations for several video and audio file types
- Registers mpc-qt with *Default Programs/Windows Settings*
- Puts mpc-qt in the "Open with" menu for all video and audio files
- Registers mpc-qt.exe so it can be used from the Run dialog and the Start Menu
- Adds mpc-qt as an AutoPlay handler for Blu-rays and DVDs
- Works when reinstalled to a different folder than the one it was in
  previously. (File associations created by the "Open with" menu have trouble
  with this.)

## What it doesn't do

- Add mpc-qt to the `%PATH%`
- Enable thumbnails for all media types (use [Icaros](http://www.majorgeeks.com/files/details/icaros.html) for this)
- Allow multiple files to be selected and opened as a playlist. This is harder
  than it sounds and it can't be done with a simple script. As a workaround,
  you can create a shortcut to mpc-qt.exe in the "Send to" menu.

## How to uninstall

To remove all traces of this script from your computer, run
`mpc-qt-assoc-uninstall.bat` as administrator.

**Note:** This is not necessary if you want to reinstall mpv later (in a
different folder, for example), only if you want to remove it completely. To
reinstall, just run `mpc-qt-assoc-install.bat` again.

## Disclaimer

Should work on Windows Vista and up, tested with Windows Vista, 7, 8.1, 10 and 11.
These scripts were written for personal use and released with the hope that
they would be useful, but without any warranty.