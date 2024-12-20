# JITStreamer-2.0
This is a JIT Enabler for iOS 17.4+ (This includes iOS 18+) over VPN (Wi-Fi only) or over Local Network / USB

## Requirements
- A Mac, Linux or Windows Computer (You can also do this with a Server but a host computer is needed to pair your device)
- A VPN such as [Tailscale](https://tailscale.com) (Wireguard based VPNs are the only ones that have been tested)
- Python 3.10+ (with pip / pip3 installed)
- `git` (on Windows you can get it [here](https://github.com/git-guides/install-git#install-git-on-windows))
- Common Sense


## Setup


Open Terminal (on Windows Administrator Powershell) and run these commands (not the ones with the #)
```
# Setup venv
python3 -m venv venv

# Activate venv 

# macOS / Linux
. ./venv/bin/activate

# Windows but using Powershell
.\venv\Scripts\Activate.ps1

# Windows but using Command Prompt/CMD 
.\venv\Scripts\Activate.bat

# Clone the Repository
git clone https://github.com/stossy11/JITStreamer-2.0.git

# cd into directory
cd JITStreamer-2.0

# Install JITStreamer
pip3 install -U -e .
(if that doesnt work try pip install -U -e . )
```



## How to use JITStreamer?
- Make sure your device is connected to a computer.
- You will need the IP of your Server / Computer from the VPN
- JITStreamer will need to be installed on that computer (if you are using a server you still need JITStreamer installed on your computer)

**Jitterbugpair paring files are not supported**

First you will need to get the pairing file from JITStreamer. 
**This will need to be run on your host computer as your device needs to be plugged in**
``` 
# Run this (in the terminal from before) and type in "y" when it asks
JITStreamer --pair
```
You should now find the file that should be a .plist file the name will correspond to your devices UDID (example: 00001111-000A1100A11101A.plist ignore the _remote plist file)

Send this file to your iDevice over AirDrop or Emailing it to yourself (Please compress the file before sending it to your iDevice)

Now you will need to connect to the VPN from before (Number 2 in Requirements) and download this shortcut on your phone: [here](https://github.com/stossy11/JITStreamer-2.0/raw/refs/heads/main/JITStreamer%202.0%20PB.shortcut)

The UDID of your device will be the name of your pairing file and the address will be the ip of your server with http:// infront (example: "http://100.97.35.58")
You will need to input your Pairing file into the shortcut.

You Will need to now launch JITStreamer on your server or Computer (make sure you are connected to the VPN on both your Server / Computer and iDevice)
```
# macOS / Linux
sudo JITStreamer

# Windows (make sure you are in an Administrator Powershell or CMD Window
JITStreamer
```

Now Run the Shortcut and you will need to press the "Upload Your Pairing File" Button and then when its done it should say `{"OK":"File uploaded"}`

Finally run the shortcut again and Enable JIT (the first time may take a while as it would be mounting your Personalised Disk Image)

# Credits

- nythepegasus for [SideJITServer](https://github.com/nythepegasus/SideJITServer)
- Jawshoeadan for the [modified pymobiledevice3 version](https://github.com/jawshoeadan/pymobiledevice3)
- doronz88 for [pymobiledevice3](https://github.com/doronz88/pymobiledevice3)
- Stossy11 for this project
- The People working on [pymobiledevice3](https://github.com/doronz88/pymobiledevice3)
- The rest of the [SideStore](https://sidestore.io) team for encouraging me!
