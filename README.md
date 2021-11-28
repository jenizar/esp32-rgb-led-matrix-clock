# esp32-rgb-led-matrix-clock
ESP32 rgb led matrix clock using p5 panel

materials:

esp32, p5 led panel (1 pcs), rtc ds3231, psu 5v/10A, jumper cable, breadboard

note: 

this program is a modified program for arduino mega 2560 modified for esp32 board.

![alt text](https://github.com/jenizar/esp32-rgb-led-matrix-clock/blob/main/screenshot/ss1.jpg)

![alt text](https://github.com/jenizar/esp32-rgb-led-matrix-clock/blob/main/screenshot/ss2.jpg)

attention:

please see file RGBmatrixPanel.cpp in the library RGB_matrix_panel, edit this line for esp32.

#if defined(ARDUINO_ARCH_SAMD) || defined(ARDUINO_ARCH_ESP32)

  // R1, G1, B1, R2, G2, B2 pins

//static const uint8_t defaultrgbpins[] = {24, 25, 26, 27, 28, 29};  //john 01.11.2021 arduino mega

//static const uint8_t defaultrgbpins[] = {2, 3, 4, 5, 6, 7};  //john 01.11.2021 arduino non-mega

<b>static const uint8_t defaultrgbpins[] = {25, 26, 27, 12, 13, 14};  //john 01.11.2021 esp32</b>

wiring hub75 pinout: (please check the program *.ino)

#define A    15

#define B    16

#define C    17

#define D    18

#define CLK  19 

#define LAT  32 

#define OE   33

RGBmatrixPanel matrix(A, B, C, D, CLK, LAT, OE, false, 64);


references:

1. https://arduino-projects-free.blogspot.com/2018/09/rgb-led-matrix-clock-with-arduino.html

2. https://www.instagram.com/p/CW0sy41hWbG/


