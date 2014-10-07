puush-screenshot
====================

A basic bash script to autoupload screenshots to Puush on Linux.

Requirements
------------

This script utillizes the following Packages:
* curl
* xclip
* gnome-screenshot
* notify-send

Make sure that all of those are installed, if you want to use the script out of the box. On most Ubuntu based distros, you only need to install xclip.

```bash
sudo apt-get update
sudo apt-get install xclip
```
Depending on your installation you might have to edit the script and change gnome-screenshot and/or notify-send to something else.

You'll also need a Puush Account.

Installation
------------

```bash
sudo curl -O https://github.com/Bujuhu/puush-autoscreenshot/puush-screenshot
sudo mv puush-screenshot /usr/local/bin/
sudo chmod +x /usr/local/puush-screenshot
```
Now you'll need your Puush API Key. You can find it on your [Puush Account Setting](http://puush.me/account/settings)

Put it directly into the Script or set up an environment variable with 
```bash
export PUUSH_API_KEY="YOUR-KEY-HERE"
```

Usage
-----
After installation you can run the script by typing 'puush-screenshot'

All Arguments parsed to the script will be forwoarded to gnome-screenshot. 
You can use all Arguments that gnome-screenshot uses, except '-f'.

To get an explanation of usable arguments type
```bash
man gnome-screenshot
```
Idealy, you would want to setup an Keyboard Shortcut.
If the Script executes sucessfully, a notification will pop up.

To change the screenshot directory and filename, change the 'DIR' and 'IMG' Variables to something else.

