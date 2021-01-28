
<p align=center>
  <img title="Built With Love" src="https://forthebadge.com/images/badges/built-with-love.svg"></p>

  <br>

<p align=center>
  <a href="https://www.instagram.com/bhikan_deshmukh"><img title="Made in INDIA" src="https://img.shields.io/badge/MADE%20IN-INDIA-SCRIPT?colorA=%23ff8100&colorB=%23017e40&colorC=%23ff0000&style=for-the-badge"></a>
  </p>

###### <p align="center"> *MapEye*

  <br>

<p align="center"><img src="res/mapeye.png"></p>

###### <p align="center">Accurate GPS Location Tracker (Android, IOS, Windows phones.)
<p align=center>
  <a href="https://www.instagram.com/bhikan_deshmukh"><img title="Open Source" src="https://img.shields.io/badge/Open%20Source-%E2%99%A5-red" ></a>
  <a href="https://www.instagram.com/bhikan_deshmukh"><img title="GitHub version" src="https://d25lcipzij17d.cloudfront.net/badge.svg?id=gh&type=6&v=1.0&x2=0" ></a>
  <a href="https://www.instagram.com/bhikan_deshmukh"><img title="Stars" src="https://img.shields.io/github/stars/bhikandeshmukh/MapEye?style=social" ></a>
  <a href="https://github.com/bhikandeshmukh/followers"><img title="Followers" src="https://img.shields.io/github/followers/bhikandeshmukh?color=blue&style=flat-square"></a>
  <a href="https://github.com/bhikandeshmukh/MapEye/network/members"><img title="Forks" src="https://img.shields.io/github/forks/bhikandeshmukh/MapEye?color=red&style=flat-square"></a>
  <a href="https://github.com/bhikandeshmukh/MapEye/watchers"><img title="Watching" src="https://img.shields.io/github/watchers/bhikandeshmukh/MapEye?label=Watchers&color=blue&style=flat-square"></a>
  <a href="#"><img src="https://badges.pufler.dev/visits/bhikandeshmukh/MapEye">

###### <p align="center">*This is official repository maintained by us*
###### <p align="center"> *[**Mr. Bee**](https://www.instagram.com/bhikan_deshmukh/) ❤️*
###### <p align="center"> *You can check [Instagram](https://www.instagram.com/bhikan_deshmukh)✌*

## MAP EYE

Concept behind mapeye.py is simple, just like we host phishing pages to get credentials why not host a fake page that requests your location like many popular location based websites. Read more on Mr. Bee's Blog mapeye.py Hosts a fake website which asks for Location Permission and if the target allows it, we can get :

* Longitude
* Latitude
* Accuracy
* Altitude - Not always available
* Direction - Only available if user is moving
* Speed - Only available if user is moving

Along with Location Information we also get **Device Information** without any permissions :

* Unique ID using Canvas Fingerprinting
* Device Model - Not always available
* Operating System
* Platform
* Number of CPU Cores - Approximate Results
* Amount of RAM - Approximate Results
* Screen Resolution
* GPU information
* Browser Name and Version
* Public IP Address
* Local IP Address
* Local Port

**Automatic IP Address Reconnaissance** is performed after the above information is received.

**This tool is a Proof of Concept and is for Educational Purposes Only, mapeye.py shows what data a malicious website can gather about you and your devices and why you should not click on random links and allow critical permissions such as Location etc.**

## How is this Different from IP GeoLocation

* Other tools and services offer IP Geolocation which is NOT accurate at all and does not give location of the target instead it is the approximate location of the ISP.

* mapeye.py uses HTML API and gets Location Permission and then grabs Longitude and Latitude using GPS Hardware which is present in the device, so mapeye.py works best with Smartphones, if the GPS Hardware is not present, such as on a Laptop, mapeye.py fallbacks to IP Geolocation or it will look for Cached Coordinates.  

* Generally if a user accepts location permsission, Accuracy of the information recieved is **accurate to approximately 30 meters**

* Accuracy depends on multiple factors which you may or may not control such as :
  * Device - Won't work on laptops or phones which have broken GPS
  * Browser - Some browsers block javascripts
  * GPS Calibration - If GPS is not calibrated you may get inaccurate results and this is very common

## Templates

Available Templates :

* NearYou
* Google Drive
* WhatsApp group
* Telegram

## Tested On :

* Kali Linux
* BlackArch Linux
* Ubuntu
* Kali Nethunter
* Termux
* Parrot OS

## Installation

### Basic For Beginners

```bash
$ git clone https://github.com/bhikandeshmukh/MapEye.git
$ cd MapEye
$ python3 mapeye.py -t manual -k testkml
```
Choose Options Batween 0 to 3

### ngrok setup

```bash
go to ngrok.com (Login)
Download ngrok
$ unzip ngrok.zip
$ ./ngrok authtoken *******
$ ./ngrok http 8080
send link to victim
```

### Kali Linux / Ubuntu / Parrot OS

```bash
git clone https://github.com/bhikandeshmukh/MapEye.git
cd MapEye
apt update
apt install python3 python3-pip php
pip3 install requests
```

### BlackArch Linux

```bash
pacman -S mapeye.py
```

### Termux

```bash
git clone https://github.com/bhikandeshmukh/MapEye.git
cd MapEye
pkg update
pkg install python php
pip3 install requests
```

## Usage

```bash
python3 mapeye.py -h

usage: mapeye.py [-h] [-s SUBDOMAIN]

optional arguments:
  -h, --help            show this help message and exit
  -k KML, --kml         Provide KML Filename ( Optional )
  -p PORT, --port       Port for Web Server [ Default : 8080 ]
  -t TUNNEL, --tunnel   Specify Tunnel Mode [ Available : manual ]

##################
# Usage Examples #
##################

# Step 1 : In first terminal
$ python3 mapeye.py -t manual

# Step 2 : In second terminal start a tunnel service such as ngrok
$ ./ngrok http 8080

###########
# Options #
###########

# Ouput KML File for Google Earth
$ python3 mapeye.py -t manual -k <filename>

# Use Custom Port
$ python3 mapeye.py -t manual -p 1337
$ ./ngrok http 1337

```

### Legal Disclaimer :

Usage of the tool for attacking targets without prior mutual consent is illegal. It's the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

-------------------------------------------------------------------------------------

### Development by

Developer / Author: [Mr. Bee](https://www.instagram.com/bhikan_deshmukh/)

###### <p align="center">To Know about Ethical Hacking , Android And Kali Linux Do ♨️ Follow ♨️ Us:-</p>
<p align="center">
<a href="https://www.instagram.com/bhikan_deshmukh/"><img title="Instagram" src="https://img.shields.io/badge/instagram-%23E4405F.svg?&style=for-the-badge&logo=instagram&logoColor=white"></a>
<a href="https://wa.me/918600525401"><img title="whatsapp" src="https://img.shields.io/badge/WHATSAPP-%2325D366.svg?&style=for-the-badge&logo=whatsapp&logoColor=white"></a>
<a href="https://www.facebook.com/thebhikandeshmukh"><img title="facebook" src="https://img.shields.io/badge/facebook-%231877F2.svg?&style=for-the-badge&logo=facebook&logoColor=white"></a>
<a href="https://www.twitter.com/bhikan_deshmukh/"><img title="twitter" src="https://img.shields.io/badge/twitter-%231DA1F2.svg?&style=for-the-badge&logo=twitter&logoColor=white"></a>
<a href="https://t.me/dev_aladdin"><img title="Telegram" src="https://img.shields.io/badge/Telegram-blue?style=for-the-badge&logo=Telegram"></a>
<a href="https://rzp.io/l/mrbee"><img title="DONATE" src="https://img.shields.io/badge/DONATE-yellow?style=for-the-badge&logo=google-pay"></a>
</p>

-------------------------------------------------------------------------------------
