# marauder-web

a simple web interface for the esp32 marauder firmware

## what is it
marauder-web is a lightweight browser ui that talks to an esp32 running **esp32 marauder** over **uart** and lets you...
* send commands to the esp32
* view the live serial output logs in-browser
* save preset commands and use a key

it uses the browser’s **web serial api**, so the page can open a serial port directly and read/write to it.

## requirements
* an esp32 running **esp32 marauder firmware**
* usb cable (esp32 <-> your computer)
* a **chromium-based browser** like chrome, edge, brave, etc. (I recommend using [ungoogled-chromium](https://github.com/ungoogled-software/ungoogled-chromium)

> note: most non-chromium browsers don’t support web serial, so the ui usually will not work there

## how it works
* plug in the esp32
* open the site (or host it yourself!)
* click connect and pick the esp32 serial port
* the app writes commands to uart and streams back the output so you can see marauder logs and responses in real time

## getting started

### 1. flash marauder
flash the esp32 with the [marauder firmware](https://github.com/justcallmekoko/ESP32Marauder) using whatever method you normally use (I recommend using [ESPressoFlash](https://espressoflash.com/) on a chromium-based browser).

### 2. use marauder-web
visit our [website](https://marauder.colasac.co) **OR** clone this repo and start it by running the following commands in the project root folder:
`npm install` (installs dependencies)
`npm run dev` (hosts the web server on your local system)
then, type `localhost:3000` into your browser's URL bar
