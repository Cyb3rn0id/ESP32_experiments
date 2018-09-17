# BLE UART OLED
How to use UART over bluetooth with Wemos Lolin 32 + oled

[![Watch example](https://img.youtube.com/vi/zz35Cp2eYmg/0.jpg)](https://www.youtube.com/watch?v=zz35Cp2eYmg)

# Step 1 - Install ESP32 for Arduino IDE
Open Arduino IDE.
In File->Settings, in the field "additional URL for board manager" add the following string:
http://arduino.esp8266.com/stable/package_esp8266com_index.json,https://dl.espressif.com/dl/package_esp32_index.json
(it is comprensive for ESP8266 and ESP32).
Press OK.
Click on Tools->Board "xyz"->Board manager
Type "ESP32", click on the result and press Install.
Wait a lot. Done.
Be sure to select "WEMOS LOLIN 32" in Tools->Board

# Step 2 - Install OLED library in Arduino IDE
Install new libraries from Sketch->#include libray->Library manager
Required libraries:
* ESP8266 and ESP32 Oled Driver for SSD1306 display by Daniel Eichorn, Fabrice Weinberg

# Step 3 - Purchase a board
I've used a Wemos Lolin32 with integrated OLED 128x64. Ebay is full.

# Step 4 - Install Terminal App
I've used Serial Bluetooth Terminal by Kai Morich, it's free and works very well.
ESP32 doesnt' require pairing, so DON'T try to pair your phone with ESP32: will not work!
You must only scan Bluetooth devices from App, then select the device you want
Then press the connect button as showed in the video above.

# Bonus: How to create XBM Images
* obtain an image, max height 64px
* convert it in BMP mono (use photoshop) and then save as BMP
* Goto: https://www.online-utility.org/image_converter.jsp
* Select XBM and press "Select Format" button
* Press "Select File", wait upload
* Press "Convert and download"
* Open XBM file, change data type to const char
