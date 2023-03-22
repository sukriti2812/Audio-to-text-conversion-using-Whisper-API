# Audio to Text conversion using Whisper API
This is an assignment done to understand how to use Whisper API from OpenAI. The dataset consists of 4 different audio clips consisting of a speech, conversations from movies, and a french song. The audio files are in the **data** folder.

## Installation

Steps to install Whisper API can be found here : https://github.com/openai/whisper

Install openai

```bash
  pip install openai
```

## Steps involved

* Whisper's medium model has been used which has 80.3% accuracy. The accuracy is determined using **WER** (Word Error Rate)
* Converted audio of file **'sample-0.mp3'** to text first simply and then using API key
* The text ouput then obtained from above has been passed to **davinci** model which completes the text with a logical response. When the temperature input is set to 0, the model generates the same output everytime it runs but when it is set to any non-zero value between 0 and 1, it returns different output.
* This text output from **davinci** model is next converted to audio using TTS library **gTTS**. This audio file is saved as **packt.mp3**.
