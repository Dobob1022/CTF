# Turning In

##### Score : 100

### Challenge

We recorded another flag... but Steve forgot to tune the radio to the proper frequency. All I hear is some music station. Come on, Steve.

rf2.iq: https://drive.google.com/file/d/1R7As6djHhA-hs2GjQByhHU2ON_jPnOR5/view?usp=sharing

This IQ file was again saved in standard GNURadio format (complex, 32bit float I, 32bit float Q)

Author: nb

---

### Description


This file is IQ format, it's basically capture some radio frequency in file. Like pcap files on Wireshark.

I used the SDR (Software Define Radio) Software, named "SDR#" but it's can't not import the IQ file directly so, It must be changed into wave file.

And I tried to covert this file into wav, to using iqToSharp to covert iq file to wav file.

![1.PNG](https://github.com/Dobob1022/CTF/blob/main/2021/Dawg%20CTF%202021/Tuning%20In/Picture_Sound/1.PNG?raw=true)

Then import into SDR# with file player plugin.

![2.PNG](https://github.com/Dobob1022/CTF/blob/main/2021/Dawg%20CTF%202021/Tuning%20In/Picture_Sound/2.PNG?raw=true)

There is few spot to get signal from noise.

But the every spot is not a flag. As you can see there is few peak point in here, and this peak point contain flag. You can see the 2 types of peak point here. Wide bandwidth is Just only Radio Station, but you can see the narrow bandwidth is the flag.

![https://raw.githubusercontent.com/Dobob1022/CTF/main/2021/Dawg%20CTF%202021/Tuning%20In/Picture_Sound/radiostation.PNG](https://raw.githubusercontent.com/Dobob1022/CTF/main/2021/Dawg%20CTF%202021/Tuning%20In/Picture_Sound/radiostation.PNG)**Radio Station Frequency** (wider than flag frequency)

![flag.PNG](https://github.com/Dobob1022/CTF/blob/main/2021/Dawg%20CTF%202021/Tuning%20In/Picture_Sound/flag.PNG?raw=true)

**Flag Station Frequency** (narrow then radio station frequency)

This challenge have hint about modulation, "FM" but SDR have 2 types of FM demodulation, NFM and WFM.

NFM is Narrow band FM, WFM is Wide band FM. but WFM have wide bandwidth, So WFM is not for this challenge. Then I use NFM to find the flag sound.

But! The sound quality so suck, I just hear the only "The Flag is". and I can't hear the flag. 
You Can here flag on this file. 

https://github.com/Dobob1022/CTF/blob/main/2021/Dawg%20CTF%202021/Tuning%20In/Picture_Sound/flag.mp3
