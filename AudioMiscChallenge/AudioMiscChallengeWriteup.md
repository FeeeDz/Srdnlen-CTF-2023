# Audio misc challenge
### Description
My friend Martin, a radio enthusiast, is on a trip to Europe. He promised me a picture of a place he liked a lot, but instead of images, he sent me only an incomprehensible audio! Can you help me, please?

The flag must be submitted in srdnlen{} format: wrap the found flag in srdnlen{}

The flag is a meaningful sentence.

## Solution
The challenge gives us a .wav file, reproducing it made sounds similar to morse code.
First, i tried ispecting the file with the *strings* command and it gave me this <br>
-mettere immagine strings <br>
**flag.png** inside it!
I tried to extract the .png with binwalk using binwalk -D=".*" challengeAudio.wav* <br>
The result was this rar file *15340C4.rar* but it was protected by a password. <br>
-mettere immagine file rar
The next step was to investigate what type of sound/protocol was reproducing the .wav file. Doing an *exiftool* to the file i found a base64 string saying
**Hint : Slow Slow Radio Transmission**.
Investingating a bit more on google i found stuff about *SSTV images in .wav files*,
> Slow-scan television (SSTV) is a picture transmission method, used mainly by amateur radio operators, to transmit and receive static pictures via radio in monochrome or color.

i followed this path and i discovered a tool called *qsstv* that helped me to decode the audio to an image. This is what i got using the software:
-mettere immagine qsstv

As you can see i got a flag in the background with a strange string. I knew right away that that string was the password for the rar archive and it was!!
Opening the .rar with that password i got the flag.png that contained the flag!
-mettere immagine flag finale

