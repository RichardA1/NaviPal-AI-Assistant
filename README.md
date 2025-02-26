# Assistive-AI-Toy
A toylike personal voice assistant for neurodiverse people.

This is ment to do medication reminders, appointments, checklists, tell stories, aid with theripy, and geniral check-ins. Basicaly this is ment to be a voice assistant companion for someone needing some help with reminders and encuragment. The idea started out as a tool for children, but many adults have expressed interest in having somthing similar.

## The goal of this project:
Design an inexpencive hardware platform that can use Text-to-speach (TTS) and Speach-to-tex (STT) combined with a Large Langage Model (LLM). This should be capable of rinning on standard 3.3V rechargable battery tech and provide simple IO interactions like buttons, LEDs, haptic motors, and other sensors for aditional interactions.

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
* Stranded wire for soldered connections. I recomend one of the following:
  - [BNTECHGO 26 Gauge Silicone Wire Kit 10 Color Each 25 ft](https://www.amazon.com/dp/B09X452TKH)
  - [BNTECHGO 28 Gauge Silicone Ribbon Cable Flexible 6P Black 20 ft Flat Cable](https://www.amazon.com/dp/B099W67FNZ)
    + *Note* the Ribbon cable will reduce the number of lose cables you have, but all cables will be black ecept for the one marked with a white stripe, typicaly indicating VCC, so this is only recomended for advanced users.
* 3 x [6x3mm round Neodymium Magnets](https://www.amazon.com/dp/B0CCXLS8QM)
* 1 x [Latching Mini ON/Off Switch](https://www.amazon.com/dp/B086L2GPGX)

## Wiering Diagram:

![This is the wireing diagram for the electronics.](https://github.com/RichardA1/Assistive-AI-Toy/blob/main/Assistive%20AI%20Toy%20-%20ESP32-S3-N8R2.png?raw=true)

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
