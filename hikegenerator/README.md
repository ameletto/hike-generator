Go on a walk without your phone where you don't know where you're going just that you'll end up where you started!

1. **Run Locally:** To run the application, use the command:
    ```
    node server.js
    ```
2. **Load Application:** Open `index.html` in a browser to use the app for generating a route.
3. **Download config.h File:** Download the `config.h` file which contains the generated route configuration.
4. **Update Arduino Code:** Replace the `config.h` file in the Arduino code directory with the newly downloaded file.

### Hardware

The hardware is based on an ESP32 device, equipped with a range of sensors for navigation and interaction.

### Components

The main components required are:

- ESP32 Feather V2 [link](https://learn.adafruit.com/adafruit-esp32-feather-v2/pinouts)
- Waveshare 1.28" Round LCD Display Module with GC9A01 Driver [link](https://www.waveshare.com/1.28inch-lcd-module.htm)
- Adafruit Push-button Power Switch [link](https://thepihut.com/products/adafruit-push-button-power-switch-breakout)
- Beitian BN 880 GPS module [link](https://store.beitian.com/products/beitian-compass-qmc5883l-amp2-6-pix4-pixhawk-gnss-gps-glonass-dual-flight-control-gps-module-bn-880q?variant=44696120295711)
- Adafruit DRV2605L Haptic Controller Breakout [link](https://learn.adafruit.com/adafruit-drv2605-haptic-controller-breakout/arduino-code)
- CMPS12 Compass [link](https://www.robot-electronics.co.uk/cmps12-tilt-compensated-magnetic-compass.html)
- Round Battery
- USB C charging port extender

### Wiring

| ESP32 Pin | Screen | Motor Driver | Compass | GPS | Push Button |
| --------- | ------ | ------------ | ------- | --- | ----------- |
| 3V        | VCC    | VIN          | VIN     | VIN |             |
| GND       | GND    | GND          | GND     | GND | GND         |
| 19 (MOSI) | DIN    |              |         |     |             |
| 4 (A5)    | RST    |              |         |     |             |
| 5 (SCK)   | CLK    |              |         |     |             |
| 12        | BL     |              |         |     |             |
| 15        | CS     |              |         |     |             |
| 32 (A7)   |        |              |         |     | OFF         |
| 33        | DC     |              |         |     |             |
| SDA       |        | SDA          | SDA     |     |             |
| SCL       |        | SCL          | SCL     |     |             |
| RX        |        |              |         | TX  |             |
| TX        |        |              |         | RX  |             |
