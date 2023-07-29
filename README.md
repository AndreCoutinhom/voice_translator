<h1 align="center">
Voice Translator
</h1>

<div style="display: inline_block"><br>
  <img align="center" alt="voice_translator" src="https://cdnb.artstation.com/p/assets/images/images/058/718/949/large/veysh-veysh-movie-still-professional-photograph-taken-with-canon-eos-855c677b-11fd-41d1-912c-b7ee86c72edc.jpg?1674809943">
  </div> 

  ###

This project was based on a video tutorial by @Ai_Austin. The repository contain Python files in wich it recieves audio in several languages - with focus on portuguese translations, since is my native language - and prompt commands for libraries installation in Shell. Besides, it uses an updated version of Google Trans API.

###


## The Video

Published in 2023 march 16th by @Ai_Austin, "Create an AI Voice Translator in 4 Minutes (Python Tutorial)", is a Python programming video tutorial that shows how to create a voice translator. The code is mainly based on python and google libraries and is runned in Visual Studio Code. The program is capable of listening to the user's voice through the machine's main audio input device, collecting a text version of the audio, translate it, and returning the translated text accompanied by a computer voice dictation. 

###

The original AI_Austin's code is set as shown below:

``` python



```


###

To watch the video, click on the Youtube rectangular red box below:

<div style="display: inline_block"><br>
  <img align="center" alt="Ai_Austin" height="350" width="350" src="https://yt3.googleusercontent.com/BIfx2QyabFvmF0KWynripygJZFq8buzPidi0VhXE3BGg-g1Xgzug4j813WiXWyhLB7LDmdyq9Gw=s900-c-k-c0x00ffffff-no-rj">
  
  <a href="https://youtu.be/oMOfN13Py84" target="_blank"><img align="center" height="95" width="350" src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" target="_blank"></a>
</div> 

## Differences between codes

There were barely none different coding structure between mine's and Austin's. In fact, the whole code was developed by watching Austin's tutorial. However, following some researches and Chat GPT's orientations through some issues I had to deal with, like code not working, bugs and syntax errors; I couldn't rely entirely on the tutorial, since some of the indicated libraries were not fully updated by the time I wrote the code myself, especially the Google trans API, responsible for the translation algorithm. That's why, on this repository, I have committed a Shell structured prompt list containing the updated version of the Google Trans API as followed below: 

```shell
pip install googletrans-py
pip install --upgrade googletrans==4.0.0-rc1
```
Besides that, AI_Austin's tutorial has a truly functional code and a much valid programming logic.

