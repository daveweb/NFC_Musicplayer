# NFC_Musicplayer
NFC/RFID NodeMCU music player(ESPHome) (with HA-NodeRed flow).
This musicplayer plays Spotify URL's to my SONOS speakers.
The NFC tagid's are mapped with the Spotify URL's in a csv file.

Used hardware
NFC_Musicplayer
- RC552 RFID reader
  https://www.bol.com/nl/p/rfid-kit-mifare-rc522-rfid-leesmodule-met-s50-witte-kaart-sleutelhanger-voor-arduino-raspberry-pi/9200000114634680/?s2a=
- ESP8266 | NodeMCU | WiFi | Arduino Development Board
  https://www.bol.com/nl/p/esp8266-nodemcu-wifi-arduino-development-board/9300000004321170/?s2a=
- Jumper cables


For assembling see https://miliohm.com/rc522-rfid-reader-with-nodemcu/
Use ESPHOME_node_nfc.yaml in ESPHOME for flashing the NodeMCU.
After flashing the NodeMCU is available in HomeAssistant

The NodeRed Flow handles the tag_scanned event.
New cards are added to /usr/share/hassio/share/tag_readertag_registration.csv
</br>
NOTE:</br>
  Make sure the file is already there with the following header:</br>
  Timestamp;TagId;Naam;URL;ContentType</br></br>
  
  
with the following line: 
  2021-02-16T17:32:25.864592+00:00;04-1A-B8-D2-E8-6B-81;Speellijst of album;spotify url;music
  
You can change the line in Excel to:</br>
2021-02-16T17:32:25.864592+00:00;04-1A-B8-D2-E8-6B-81;Fleedwood Mac - Rumours;spotify:album:1bt6q2SruMsBtcerNVtpZB;music


In my case the card remains on the tag reader while playing. 
to stop playing: simply remove the card from the reader and the music will stop in 5 seconds.
You need something to keep the card in place(eg. wooden ledge).

Music is played to my SONOS

- RaspberryPi 4b 
Installed with Raspbian, docker Homeassistant, Node Red




