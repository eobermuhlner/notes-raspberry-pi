# notes-raspberry-pi
Notes about setting up and using a Raspberry Pi

# Hardware

## Raspberry Pi Zero

The Raspberry Pi Zero uses mini HDMI and Micro USB connectors.
This means you can probably not simply plug in your normal HDMI cable or keyboard/mouse.

- USB OTG Host Cable
- mini HDMI male to HDMI female Adapter

# Setup

## Enable SSH

In Desktop Click
  - menu: Raspberry Icon/Preferences/Raspberry Pi Configuration
  - tab: Interfaces
  - SSH radiobutton: Enable
  - button: OK

## Fix IP address

Source: https://thepihut.com/blogs/raspberry-pi-tutorials/how-to-give-your-raspberry-pi-a-static-ip-address-update

Source: https://www.ionos.com/digitalguide/server/configuration/provide-raspberry-pi-with-a-static-ip-address

Add to `/etc/dhcpcd.conf`:
```
interface eth0

static ip_address=192.168.0.11/24
static routers=192.168.0.1
static domain_name_servers=192.168.0.1 8.8.8.8

interface wlan0

static ip_address=192.168.0.211/24
static routers=192.168.0.1
static domain_name_servers=192.168.0.1 8.8.8.8
```




