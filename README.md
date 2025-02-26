# Assistive-AI-Toy
A toy-like personal voice assistant for neurodiverse individuals.

This device is designed to provide medication reminders, schedule appointments, manage checklists, tell stories, support therapy, and offer general check-ins. Essentially, it serves as a voice assistant companion for individuals who need help with reminders and encouragement. While the idea originally started as a tool for children, many adults have expressed interest in something similar.

[![YouTube](http://i.ytimg.com/vi/SLpDSxgNKxc/hqdefault.jpg)](https://www.youtube.com/watch?v=SLpDSxgNKxc)

## Project Goal
The goal of this project is to design an inexpensive hardware platform that integrates Text-to-Speech (TTS) and Speech-to-Text (STT) with a Large Language Model (LLM). The device should run on a standard 3.3V rechargeable battery and support simple I/O interactions, including buttons, LEDs, haptic motors, and additional sensors for enhanced interactions.

## Prototype Parts List:

* 1 x [ESP32-S3-N8R2](https://www.amazon.com/dp/B0B6HT7V7P)
* 1 x [INMP441 I2S MEMS Microphone Module](https://www.amazon.com/dp/B09G4RNT3G)
* 1 x [Max98357 I2S 3W Class D Amplifier](https://www.amazon.com/dp/B0B4GK5R1R)
* 1 x [4Ohm 40mm Diameter 3W Full Range Audio Speaker](https://www.amazon.com/dp/B01LN8ONG4)
* 1 x [12x12x8mm Momentary Tactile Push Button Switch](https://www.amazon.com/dp/B07HBQFJ1W)
* 1 x [NeoPixel Ring - 16 x 5050 RGB LED](https://www.amazon.com/dp/B08XWFTJQ8)
* 1 x [Adafruit PowerBoost 1000 Charger](https://www.amazon.com/dp/B01BMRBTH2)
* 1 x [3.7V 3000mAh Lithium Battery](https://www.amazon.com/dp/B0BG7ZTJSR)
* 1 x [2 Pin Magnetic Connector (male)](https://www.amazon.com/dp/B0CSX6ZQ1H)
* 1 x [2 Pin Magnetic USB Charging Cable](https://www.amazon.com/dp/B0BV2RF5N4)
* Stranded wire for soldered connections. I recommend one of the following:
  - [BNTECHGO 26 Gauge Silicone Wire Kit 10 Color Each 25 ft](https://www.amazon.com/dp/B09X452TKH)
  - [BNTECHGO 28 Gauge Silicone Ribbon Cable Flexible 6P Black 20 ft Flat Cable](https://www.amazon.com/dp/B099W67FNZ)
    + *Note* the Ribbon cable will reduce the number of lose cables you have, but all cables will be black except for the one marked with a white stripe, typically indicating VCC, so this is only recommended for advanced users.
* 3 x [6x3mm round Neodymium Magnets](https://www.amazon.com/dp/B0CCXLS8QM)
* 1 x [Latching Mini ON/Off Switch](https://www.amazon.com/dp/B086L2GPGX)

## Wiering Diagram:

![This is the wireing diagram for the electronics.](/Assistive%20AI%20Toy%20-%20ESP32-S3-N8R2.png)

### Pin Mapping:

Here is the pin mapping table:

| INMP441 Microphone  |     Speaker    | LED Strip WS2812B  | Input Switch  | Boost 1000  |
|      :---:          |   :---:        |         :---:      |     :---:     |   :---:     |
| GPIO 4 --> SD       | GPIO 8 --> DIN |   GPIO 9 --> Din   |    GPIO 10    | 5V --> 5V   |
| GPIO 3 --> WS       | GPIO 6 --> LRC |                    |               |             |
| GPIO 2 --> SCK      | GPIO 7 -> BLCK |                    |               |             |
| 3v3 --> VDD         | 3v3 --> Vin    | Vin  --> (5v)Vin   |               |             |
| GND --> GND & L/R   | GND --> Gnd    | GND --> GND        | GND           | GND --> GND |

## 3D Print files:

Here are all the 3D print files.
* [NaviPal (main body).stl](/STL%20Files/NaviPal%20(main%20body).stl)
* [NaviPal (face).stl](/STL%20Files/NaviPal%20(face).stl)
* [NaviPal (LED plate).stl](/STL%20Files/NaviPal%20(LED%20plate).stl)
* [NaviPal (LED diffuser).stl](/STL%20Files/NaviPal%20(LED%20diffuser).stl)

Push Text-to-speach (TTS) to the speaker:
Here is an axsample fo the YAML code for simple text to speach:
```yaml
action: tts.speak
data:
  message: It is time #The message you want to send
  language: en-US
  media_player_entity_id: media_player.boo #The media player you want to target
  options:
    voice: DavisNeural #This is for the voice you want to use
target:
  entity_id: tts.home_assistant_cloud
```

You can also use templates in the "message:" section:
```yaml
data:
  message: It is {{ now().strftime('%-I:%M %p') }}
```
