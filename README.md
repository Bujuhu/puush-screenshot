puush-screenshot
====================

A basic bash script to auto-upload screenshots to Puush on Linux.

Requirements
------------

This script utilizes the following Packages:
* curl
* xclip
* scrot
* notify-send

Make sure that all of those are installed, if you want to use the script out of the box. On most Ubuntu based distros, you only need to install xclip.

```bash
sudo apt-get update
sudo apt-get install xclip
```
Depending on your installation you might have to edit the script and change scrot to something else.

You'll also need a Puush Account.

Installation
------------

```bash
sudo curl -O https://raw.githubusercontent.com/Bujuhu/puush-screenshot/master/puush-screenshot
sudo mv puush-screenshot /usr/local/bin/
sudo chmod +x /usr/local/bin/puush-screenshot
```

To use this Script you need your Puush API Key, which can be found in the [Puush Account Settings Page](http://puush.me/account/settings)

Put it directly into the Script or set an environment variable by putting this is in your `~/.bash_profile` or equivalent
```bash
export PUUSH_API_KEY="YOUR-KEY-HERE"
```

Usage
-----
After installation you can run the script using the 'puush-screenshot' keyword

All Arguments parsed to the script will be forwarded to gnome-screenshot.
You can use all Arguments that scrot uses.

To get an explanation of usable arguments type
```bash
man scrot
```

To change the screenshot directory and filename, change the 'SCREENSHOT_DIR' and 'SCREENSHOT_FILE' Variables to something else, either also als enviroment Variable or inside Script
