# ESP32-Camera-Server
This is a ESP32 Camera Server with Mail client, and using Bluetooth base remote control method to captue photo and send to an email address.

## Board 
[ESP32-CAM with OV2640 Camera Module](https://makeradvisor.com/tools/esp32-cam/)

[HC05](https://www.amazon.com/DSD-TECH-HC-05-Pass-through-Communication/dp/B01G9KSAF6)
## Setup Hardware env

### Connect ESP32-CAM with Arduino UNO
Since this board don't has Micro-USB serial console so you need to use on board RX TX port to connet to PC by using Arduino UNO.

Please check [this blog](https://kerwenwwer.notion.site/Using-Arduino-UNO-connect-to-ESP32-Cam-35d9be114a8e44ef94520fbc46b82f21)


## Package requestment
* WiFi
* SPI
* ESP32_MailClient
* FS


## Usage 
Replace this variable to your own setting in  ``CameraWebServer.ino``
```=c
// To send Emails using Gmail on port 465 (SSL), you need to create an app password: https://support.google.com/accounts/answer/185833
#define emailSenderAccount    "Your Email Account "
#define emailSenderPassword   "Your Email Account password"
// If you use Gmail that will be "smtp.gmail.com"
#define smtpServer            "smtp.office365.com"
#define smtpServerPort        587
#define emailSubject          "ESP32-CAM Photo Captured"
#define emailRecipient        "Your Target mail address"
#define WiFiSSID              "Your WiFi SSID"
#define WiFIPassword          "Your WiFi Password"
```
Then using Arduino to upload fireware to ESP32-CAM board and using another HC-50 board to send the capture singal.
