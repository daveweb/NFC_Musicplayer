# NFC_Musicplayer
NFC/RFID NodeMCU music player(ESPHome) (with HA-NodeRed flow)

Used hardware
NFC_Musicplayer
- RC552 RFID reader
  https://www.bol.com/nl/p/rfid-kit-mifare-rc522-rfid-leesmodule-met-s50-witte-kaart-sleutelhanger-voor-arduino-raspberry-pi/9200000114634680/?s2a=
- ESP8266 | NodeMCU | WiFi | Arduino Development Board
  https://www.bol.com/nl/p/esp8266-nodemcu-wifi-arduino-development-board/9300000004321170/?s2a=
- Jumper cables


for assembling see https://miliohm.com/rc522-rfid-reader-with-nodemcu/
Use ESPHOME_node_nfc.yaml in ESPHOME for flashing the NodeMCU
After flashing the NodeMCU is available in HomeAssistant

The NodeRed Flow handles the tag_scanned event.
New cards are added to /usr/share/hassio/share/tag_readertag_registration.csv
Make sure the file is already there with the following header:

Timestamp;TagId;Naam;URL;ContentType


- RaspberryPi 4b 
Installed with Raspbian, docker Homeassistant, Node Red




