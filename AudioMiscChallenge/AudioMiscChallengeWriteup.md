# Audio misc challenge
### Description
My friend Martin, a radio enthusiast, is on a trip to Europe. He promised me a picture of a place he liked a lot, but instead of images, he sent me only an incomprehensible audio! Can you help me, please?

The flag must be submitted in srdnlen{} format: wrap the found flag in srdnlen{}

The flag is a meaningful sentence.

## Solution
The challenge gives us a .wav file, reproducing it made sounds similar to morse code.
First, i tried ispecting the file with the *strings* command and it gave me this <br>
![Screenshot from 2023-10-28 17-09-06](https://github.com/FeeeDz/Srdnlen-CTF-2023/assets/67475596/7a9372e5-2aa5-4028-8e23-834a1e370e12)

**flag.png** inside it!
I tried to extract the .png with binwalk using binwalk -D=".*" challengeAudio.wav* <br>
The result was this rar file *15340C4.rar* but it was protected by a password. <br>
![Screenshot from 2023-10-29 20-37-36](https://github.com/FeeeDz/Srdnlen-CTF-2023/assets/67475596/53b1c254-f360-4430-b77c-e9753964b933)

The next step was to investigate what type of sound/protocol was reproducing the .wav file. Doing an *exiftool* to the file i found a base64 string saying
**Hint : Slow Slow Radio Transmission**.
Investingating a bit more on google i found stuff about *SSTV images in .wav files*,
> Slow-scan television (SSTV) is a picture transmission method, used mainly by amateur radio operators, to transmit and receive static pictures via radio in monochrome or color.

i followed this path and i discovered a tool called *qsstv* that helped me to decode the audio to an image. This is what i got using the software:
![Screenshot from 2023-10-28 17-24-54](https://github.com/FeeeDz/Srdnlen-CTF-2023/assets/67475596/fa4e50bc-a5b4-4576-bd7b-cfd6628269a2)

As you can see i got a flag in the background with a strange string. I knew right away that that string was the password for the rar archive and it was!!
Opening the .rar with that password i got the flag.png that contained the flag!
![Screenshot from 2023-10-28 17-42-40](https://github.com/FeeeDz/Srdnlen-CTF-2023/assets/67475596/5e78740d-a120-4e30-8864-83bb29afdf2e)


