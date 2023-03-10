# ESP32 DDoS Detector

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This is an ESP32 code that can detect a DDoS attack by monitoring incoming network traffic and analyzing it for anomalies. The code uses the ESPAsyncWebServer library to monitor incoming network traffic and statistical analysis techniques such as mean and standard deviation to identify patterns that indicate a DDoS attack. Once a DDoS attack is detected, the code takes action to prevent it from affecting the system.

## Getting Started

### Prerequisites

To run this code, you need:

* An ESP32 development board
* The Arduino IDE installed on your computer
* The ESPAsyncWebServer library installed in the Arduino IDE

### Installing

1. Clone this repository to your local machine using this command:
git clone https://github.com/Scroll-down/Esp32-ddos-detection.git
2. Open the "ddos_detector.ino" file in the Arduino IDE.
3. Compile and upload the code to your ESP32 board.

## Usage

1. Connect your ESP32 board to your network.
2. Open the Serial Monitor in the Arduino IDE.
3. Monitor the incoming network traffic in real-time using the ESPAsyncWebServer library.
4. Analyze the traffic for anomalies using statistical analysis techniques such as mean and standard deviation.
5. Set a threshold for what is considered normal traffic.
6. Once a DDoS attack is detected, take action to prevent it from affecting the system.

## How it Works

This code sets the threshold to 100 and monitors the incoming network traffic using the `server.client()->available()` function. It then calculates the mean and standard deviation of the request size and compares it to the threshold. If the incoming traffic exceeds the threshold and the request size is more than two standard deviations from the mean, then the code assumes a DDoS attack and takes action to prevent it from affecting the system.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Acknowledgments

* The ESPAsyncWebServer library
* The Arduino IDE
* The ESP32 development board.
