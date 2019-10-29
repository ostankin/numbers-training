# numbers-training

## About

A simple Javascript page to practice recognizing Estonian spoken numbers.
Click `Uus number` or hit `Esc` to start, or to generate a new number.
Type the number you hear, then hit `Enter`. To listen again,
click `Kuula uuesti`. To show the correct answer, click `Vaata õige vastus`.

Numbers are generated randomly in the range between `0` and `99`.

# Improvement plans

* Add an option to train hundreds and thousands
* Extract page formatting into a CSS
* Add more languages

# Voice files

Voice files have been generated using [Google Text-to-Speech](https://pypi.org/project/gTTS/)
Python library:

```
from gtts import gTTS
lang = 'et'
[gTTS(text=str(i), lang=lang).save('{}/{}.mp3'.format(lang,i)) for i in range(0,100)]
```