# marauder-web

a simple web interface for the esp32 marauder firmware

## what it is
marauder-web is a lightweight browser ui that talks to an esp32 running **esp32 marauder** over **uart** and lets you...
send commands to the esp32
view the live serial output logs in-browser
save preset commands and use a key

it uses the browser’s **web serial api**, so the page can open a serial port directly and read/write to it.

## requirements
- an esp32 running **esp32 marauder firmware**
- usb cable (esp32 ↔ your computer)
- a **chromium-based browser** (chrome, edge, brave, etc)

> note: most non-chromium browsers don’t support web serial, so the ui may not work there

## how it works
- you plug in the esp32
- open the site locally (or hosted)
- click connect and pick the esp32 serial port
- the app writes commands to uart and streams back the output so you can see marauder logs and responses in real time

## getting started

### 1 flash marauder
flash the esp32 with the esp32 marauder firmware using whatever method you normally use (prebuilt binary / platformio / flasher).

### 2 run marauder-web
clone this repo and start it like any small web project

```bash
git clone <your-repo-url>
cd marauder-web
# then use your preferred dev server (examples below)
