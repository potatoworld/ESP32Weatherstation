# ESP32Weatherstation
**A coding practice project using an ESP329+TFT ST7735 to display basic weather information pulled from OpenWeatherMap API**

Disclaimer: The entirity of this code was generated by GPT4, and majority of this readme/guide was generated by ChatGPT. This project was a personal exploration into using GPT to create the code for my personal projects as I lack coding skills, but have design/maker skills. As such, please vet the code and install guide yourself, as there may be inaccuracies.

Also, yes. The progress bar is hard coded to take 4 seconds, purely for aesthetics.

The Case was designed in Fusion360 and does not require any tools to put together. The screen will clip in and be held in place, the ESP32 should be held in with a small piece of double sided tape. The lid should press fit in place as well. I printed mine in CF-PETG on a Bambu Labs P1S.

![IMG_3623](https://github.com/potatoworld/ESP32Weatherstation/assets/37276609/7d703d57-8970-4f28-890d-5677bccf6ad1)

# (GPT) Intro and parts list:

This project presents an ESP32-powered weather station, a practical and educational tool designed for enthusiasts in electronics, programming, and weather monitoring. It's an open-source, DIY project that provides real-time weather updates by fetching data from the OpenWeatherMap API. The main goal of this project is to create a compact, efficient, and user-friendly device that displays weather information clearly and accurately.

**Features**

Real-Time Weather Data: Utilizes the OpenWeatherMap API to display current weather conditions, temperature, and precipitation forecasts.
ESP32 Microcontroller: Leverages the power of the ESP32 for WiFi connectivity and robust data processing.
TFT Display: Incorporates an Adafruit ST7735 TFT display for vivid and clear presentation of weather data.
User Interface: Features a simple and intuitive display layout with centered text and a WiFi connection progress bar.
Portrait Mode Orientation: Optimizes screen space and enhances readability.
Power Efficiency: Designed with a focus on low power consumption for extended use.
Customizable: Open to modifications and customizations in both hardware and software aspects.


**Ideal for:**

Home weather monitoring
Educational purposes in schools or workshops
Hobby projects for learning IoT, microcontroller programming, and API integration
Tech enthusiasts interested in building their own weather stations

**Electronics Parts List**

ESP32 Development Board: Acts as the brain of the station, providing WiFi capabilities and data processing.
Adafruit ST7735 TFT Display: A compact display for outputting weather data.
Breadboard: For prototyping and making connections without soldering.
Jumper Wires: To connect the ESP32 with the TFT display.
Micro USB Cable: For powering the ESP32 board.
Optional Battery Pack: For making the device portable.

**Setup and Usage**

This project requires basic knowledge of electronics assembly and programming. The user needs to set up the ESP32 board, connect it to the TFT display, and program it using the provided Arduino code. The code includes functions for connecting to WiFi, fetching data from the OpenWeatherMap API, and displaying the information on the screen. Users need to obtain their own API key from OpenWeatherMap and input their WiFi credentials to get started.

This project is a great way to delve into the world of IoT and embedded systems, providing a hands-on experience in interfacing hardware with web APIs and creating a practical, everyday-use gadget*

**Contribution and Collaboration**

Contributions to the project are welcome, whether they involve improvements to the code, suggestions for hardware enhancements, or documentation updates. This project is intended to be a collaborative and evolving platform for learning and innovation in the field of IoT and weather monitoring.

# (GPT) Software install guide:

This guide will walk you through the software setup required for the ESP32-Powered Weather Station project. You will need to install several software tools and libraries, and then upload (flash) the provided code to your ESP32 board.

**Prerequisites**

Basic knowledge of electronics and programming.
Access to a computer with an internet connection.

**Step 1:** Install Arduino IDE
The Arduino Integrated Development Environment (IDE) is used for writing and uploading code to the ESP32 board.

Download Arduino IDE: Visit the Arduino Software page and download the appropriate version for your operating system (Windows/Mac/Linux).

Install Arduino IDE: Run the downloaded installer and follow the installation instructions.

**Step 2:** Install ESP32 Board in Arduino IDE

After installing the Arduino IDE, you need to add support for the ESP32 board.

Open Arduino IDE.
Go to File > Preferences.
In the "Additional Board Manager URLs" field, enter the following URL:

https://dl.espressif.com/dl/package_esp32_index.json

Click "OK".

Go to Tools > Board > Boards Manager.

In the Boards Manager, search for "ESP32" and install the latest version of the "ESP32 by Espressif Systems".

**Step 3:** Install Required Libraries
Several libraries are needed for this project, including those for the TFT display and JSON parsing.

Open Arduino IDE.

Go to Sketch > Include Library > Manage Libraries.

In the Library Manager, search for and install the following libraries:

*  Adafruit GFX Library 

* Adafruit ST7735 and ST7789 Library

* ArduinoJson

**Step 4:**  Prepare the Code

Download the Project Code: The code for the ESP32 Weather Station can be found on the project's GitHub page.

Extract the downloaded code to a known location on your computer.

**Step 5:** Configure the Code
Open the Arduino IDE.

Open the downloaded code (File > Open and navigate to the code location).

Modify the code to include your WiFi credentials and OpenWeatherMap API key.

**Step 6:** Connect the ESP32 to Your Computer

Using a Micro USB cable, connect the ESP32 board to your computer.

**Step 7:** Flash the Code to the ESP32

In the Arduino IDE, select the correct board and port:

Go to Tools > Board and select "ESP32 Dev Module".

Go to Tools > Port and select the port that your ESP32 is connected to.

Click the upload button (right arrow icon) in the Arduino IDE to compile and upload the code to the ESP32.

**Step 8:** Verify Operation

Once the code is uploaded:

The ESP32 will attempt to connect to WiFi.

Upon successful connection, it will fetch weather data and display it on the TFT screen.


Troubleshoot any issues by checking the serial monitor in the Arduino IDE (Tools > Serial Monitor).
Support and Troubleshooting

For additional support and troubleshooting, refer to the project's GitHub repository or the Arduino community forums.

By following these steps, your ESP32-Powered Weather Station should be up and running, providing real-time weather updates. Enjoy your journey into the world of IoT and embedded programming!

# Pinout

**ESP32 to Adafruit ST7735 TFT Display Pinout:**

TFT Display VCC (Power) - Connect to ESP32 3.3V.

TFT Display GND (Ground) - Connect to ESP32 GND.

TFT Display CS (Chip Select) - Connect to ESP32 GPIO 5 (as defined by #define TFT_CS 5).

TFT Display RST (Reset) - Connect to ESP32 GPIO 4 (as defined by #define TFT_RST 4).

TFT Display DC (Data/Command) - Connect to ESP32 GPIO 2 (as defined by #define TFT_DC 2).

TFT Display MOSI (Master Out Slave In) - Connect to ESP32 GPIO 23 (as defined by #define TFT_MOSI 23).

TFT Display SCLK (Serial Clock) - Connect to ESP32 GPIO 18 (as defined by #define TFT_SCLK 18).

TFT Display BL (Backlight, if available) 
