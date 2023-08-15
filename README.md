<h1 align="center">
Voice Translator 
</h1>

<h1 align="center">
  <img align="center" alt="lab" height="70" width="70" src="https://images.vexels.com/media/users/3/166477/isolated/lists/9bb722f0e85ddbc1ce0f064534fd2311-icone-da-linguagem-de-programacao-python.png">

</h1>

<div style="display: inline_block"><br>
  <a href="https://www.artstation.com/artwork/qQ4y5D" target="_blank"><img align="center" alt="voice_translator" src="https://cdnb.artstation.com/p/assets/images/images/058/718/949/large/veysh-veysh-movie-still-professional-photograph-taken-with-canon-eos-855c677b-11fd-41d1-912c-b7ee86c72edc.jpg?1674809943"></a>
  </div> 

  ###

This project was based on a video tutorial by @Ai_Austin. The repository contain Python files in wich it recieves audio in several languages - with focus on portuguese translations, since is my native language - and prompt commands for libraries installation in Shell. Besides, it uses an updated version of Google Trans API.

###


## The Video 📽️

Published in 2023 march 16th by @Ai_Austin, "Create an AI Voice Translator in 4 Minutes (Python Tutorial)", is a Python programming video tutorial that shows how to create a voice translator. The code is mainly based on python and google libraries and is runned in Visual Studio Code. The program is capable of listening to the user's voice through the machine's main audio input device, collecting a text version of the audio, translate it, and returning the translated text accompanied by a computer voice dictation. 

###

The original AI_Austin's code is set as shown below:

``` python

import speech_recognition as sr
import pyttsx3
from langdetect import detect
from googletrans import Translator

# create a recognizer object, a translator object and a Text-to-Speech object

r = sr.Recognizer()
translator = Translator(service_urls=['translate.google.com'])
tts = pyttsx3.init()

while True:
    # use the default microphone as the audio source
    with sr.Microphone() as source:
        print("Speak something...")
        # adjust the ambient noise level
        r.adjust_for_ambient_noise(source)
        # listen for audio input from the user
        audio = r.listen(source)
    try:
        # recognize speech using Google Speech Recognition 
        text = r.recognize_google(audio)
        input_language = detect(text)
        # translate speech to English if detected language is Spanish
        if input_language == "es":
            translation = translator.translate(text, dest='en')
            print(f"Translated to English: {translation.text}")
            # speak the translated text
            tts.say(translation.text)
            tts.runAndWait()
        # translate speech to Spanish if detected language in English
        elif input_language == "en":
            translation = translator.translate(text, dest='es')
            print(f"Translated to Spanish: {translation.text}")
            # speak the translated text
            tts.say(translation.text)
            tts.runAndWait()
        else:
            print("Unsupported language")
    except sr.UnknownValueError:
        print("Google Speech Recognition could not understand audio.")
    except sr.RequestError as e:
        print("Could not request results from Google Speech Recognition service: {e}")

```


###

## Austin Dobbins' Github and Youtube Channel 🤖

<div style="display: inline_block"><br>
  <img align="center" alt="Ai_Austin" height="250" width="250" src="https://avatars.githubusercontent.com/u/128954893?v=4">

  <a href="https://github.com/Ai-Austin" target="_blank"><img align="center" height="37" width="123" src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=purple" target="_blank"></a>
  <a href="https://www.youtube.com/@Ai_Austin" target="_blank"><img align="center" height="33" width="123" src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" target="_blank"></a>
</div> 

## Differences between codes 👨‍💻

There were barely none different coding structure between mine's and Austin's. In fact, the whole code was developed by watching Austin's tutorial. However, following some researches and Chat GPT's orientations through some issues I had to deal with, like code not working, bugs and syntax errors; I couldn't rely entirely on the tutorial, since some of the indicated libraries were not fully updated by the time I wrote the code myself, especially the Google trans API, responsible for the translation algorithm. That's why, on this repository, I have committed a Shell structured prompt list containing the updated version of the Google Trans API as followed below: 

```shell
pip install googletrans-py
pip install --upgrade googletrans==4.0.0-rc1
```
Besides that, AI_Austin's tutorial has a truly functional code and a much valid programming logic.

## Innovative Potentials 🧠

On a bright future, I would like to investigate ways to use this kind of software into corporate tech solutions. I imagine a device with an audio and visual interface that can be used to instantly translate what people are saying. This innovative solution can bring wonders for international relationships professionals.

