generates raw audio data in s16le at your sampling frequency of choice (default: 8khz)

for now the output is mono, single voice, only staccato

supports:
- notes and chords
- variable duration for notes or chords
- arbitrary sampling rates
- adsr envelopes
- harmonics



demo: https://vocaroo.com/1lXQGtfiTt7t



examples:

```
$ ./music.bash  # play a test song

$ inter=250 ./music.bash e5 ds5 e5 ds5 e5 b4 d5 c5 a4:300 # play fur elise

$ samples=441000 ./music.bash your notes here |
  lame -r -s 44.1 --signed -m m --noreplaygain - song.mp3
```
