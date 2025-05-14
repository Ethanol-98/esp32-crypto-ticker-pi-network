# ESP32 Crypto Ticker - Pi Network

A simple ESP32 project that displays the real-time price of Pi Network (PI) in USD using a 1.14" ST7789 TFT screen. Data is fetched from CoinGecko every 30 seconds.

## Features
- Displays current PI price in USD
- Shows percent change over 5 minutes and 1 hour
- Automatic WiFi reconnection
- Clean, color-coded display

## Hardware Requirements
- ESP32 development board
- 1.14" ST7789 TFT display (135×240 resolution)
- USB cable
- Jumper wires or headers

## Wiring (Default GPIO)

| ST7789 Pin | ESP32 GPIO |
|------------|------------|
| VCC        | 3.3V       |
| GND        | GND        |
| SCL        | 18         |
| SDA        | 23         |
| RES        | 4          |
| DC         | 2          |
| CS         | 15         |

Update the pin assignments in `crypto_ticker.ino` if needed.

## Libraries Used
Install these via Arduino Library Manager:
- `WiFi`
- `WiFiClientSecure`
- `HTTPClient`
- `ArduinoJson`
- `Adafruit GFX`
- `Adafruit ST7789`

## Setup
1. Clone or download this repository.
2. Open `src/crypto_ticker.ino` in Arduino IDE.
3. Update the WiFi credentials:
   ```cpp
   const char* WIFI_SSID = "YOUR_WIFI_NAME";
   const char* WIFI_PASS = "YOUR_WIFI_PASSWORD";
   	4.	Connect your ESP32 board.
	5.	Select the correct board and port in Arduino IDE.
	6.	Upload the code.
	7.	Watch the display update every 30 seconds!
