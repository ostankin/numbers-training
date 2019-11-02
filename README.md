# numbers-training

## About

A simple [Javascript page](https://ostankin.github.io/numbers-training/)
to practice recognizing Estonian spoken numbers.
Click `Uus number` or hit `Esc` to start (also to generate a new number).
Type the number you hear, then hit `Enter` or click `Kontrolli`.
To listen again, click `Kuula uuesti`. To show the correct answer, click `?`.

Numbers are generated randomly in the range between `0` and `99`.

# Improvement plans

* Add an option to train hundreds and thousands
* Add more languages
* Introduce ordinal numbers

# Voice files

Voice files have been generated using [Google Text-to-Speech](https://pypi.org/project/gTTS/)
Python library:

```
from gtts import gTTS
lang = 'et'
[gTTS(text=str(i), lang=lang).save('{}/{}.mp3'.format(lang,i)) for i in range(0,100)]
```
