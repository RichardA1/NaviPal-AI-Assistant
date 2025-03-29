# 🤖 Meet NaviPal: The Reminder Robot For All

<img src="https://github.com/rexsaurus/NaviPal/blob/main/D1AF2927-EC39-4FAE-AD07-F49C783F85D4.jpeg?raw=true" width="350"/>

Hello everyone, my name is Richard Albritton, inventor and creator of NaviPal, the friendly open-source, low-cost robot reminder pal. I am launching a couple memecoins simultaneously on Solana and Binance to help fund the development of my vision: A simple, easy to use robot reminder friend for kids, neurodiverse adults and ... well ... everyone. 

I built NaviPal to help my husband remember to take her pills. It worked so well, many people have asked me to keep working on the project and turn it into a product anyone can use. My vision is to finance NaviPal via launching memecoins and to use the proceeds to build an open-source friendly robot factory. 

## What are the benefits of a robot reminder pal?

💊 Need to remember to take your pills? I got you covered

🕑 Have an appointment? I will remind you

📣 Program me with your voice. Press a button, tell me what you want me to remind you of (and when) and I will do so automatically with AI

🪥🦷 I can remind kids to brush their teeth at 8am and at 7pm, all with a push of a button

You can "program" NaviPal simply by pressing a button and speaking to it. On-board AI will automatically figure out what to remember and remind you at the right time. It's simple, cheap and easy. 

# Watch The Demo

[![YouTube](http://i.ytimg.com/vi/SLpDSxgNKxc/hqdefault.jpg)](https://www.youtube.com/watch?v=SLpDSxgNKxc)

Take a moment to watch me walk through a demo of how NaviPal works. 

 🥰 Meet NaviCoin: A Meme for Robo-Friends



Building robo friends takes time, materials, workshops, tools and soldering iron and love! So we thought it would be swell to launch my very own coin on Solana and Binance. NaviCoin represents pure robot love energy, it is like an electric hug 🥰🫂 right inside your wallet. I hold 40% of supply, will sell some to pay for develolment and hold some for later. NaviCoin has no utility, its justa meme friends.

Binance address:
Solana address: 

# Follow Us On Socials

Make sure to join our community. we are recruiting robot builders, open source contributors, software developers and designers. or if you just wanna hang out, thats fine too!

Follow Richard on X: 
Join us on Telegram:

# About Richard Albritton

Bio 

# Roadmap

We are currently doing a little bit of a memecoin launch on Solana and Binance to spread awareness of the project. Once we are done, our plan is to go big! We will add tons of features, listen to the community and ultimately ship robots to those who order them. Thats a widdle ways off, but we will get there soon!

# Our History

Richard built me because his husband keeps forgetting things. What better way to stay healthy than having your own robot pal? Well guess what - it turns out lots of people want one too! so richard decided to open source me and turn me loose! 

This device is designed to provide medication reminders, schedule appointments, manage checklists, tell stories, support therapy, and offer general check-ins. Essentially, it serves as a voice assistant companion for individuals who need help with reminders and encouragement. While the idea originally started as a tool for children, many adults have expressed interest in something similar.



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
