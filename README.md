# Assistive-AI-Toy
A toylike personal voice assistant for neurodiverse people.

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
