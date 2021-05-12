# Turning In

##### Score : 100

### Problem

We recorded another flag... but Steve forgot to tune the radio to the proper frequency. All I hear is some music station. Come on, Steve.

rf2.iq: https://drive.google.com/file/d/1R7As6djHhA-hs2GjQByhHU2ON_jPnOR5/view?usp=sharing

This IQ file was again saved in standard GNURadio format (complex, 32bit float I, 32bit float Q)

Author: nb

---




This file is IQ format, it's basically capture some radio frequency in file. Like pcap files on Wireshark.

I used the SDR (Software Define Radio) Software, and I used SDR# but it's can't not import the IQ file so, it must be changed into wave file.

And I tried to covert this file into wav, using iqToSharp to covert iq file to wav file.

![1.PNG](https://github.com/Dobob1022/CTF/blob/main/2021/Dawg%20CTF%202021/Tuning%20In/Pictures/1.PNG?raw=true)

Then import into SDR# with file player plugin.

![2.PNG](https://github.com/Dobob1022/CTF/blob/main/2021/Dawg%20CTF%202021/Tuning%20In/Pictures/2.PNG?raw=true)

There is few spot to get signal from noise.

![radiostation.PNG](https://github.com/Dobob1022/CTF/blob/main/2021/Dawg%20CTF%202021/Tuning%20In/Pictures/radiostation.PNG?raw=true)

But the spot is not a flag. As you can see there is a small bandwidth graph on there, that's the flag.

![flag.PNG](https://github.com/Dobob1022/CTF/blob/main/2021/Dawg%20CTF%202021/Tuning%20In/Pictures/flag.PNG?raw=true)

But! The sound quality so suck, I just hear the only "The Flag is". and I can't hear the flag. 
You Can here flag on this file. 

[flag.mp3](https://github.com/Dobob1022/CTF/blob/main/2021/Dawg CTF 2021/Tuning In/Picture_Sound/flag.mp3)



That was so close...