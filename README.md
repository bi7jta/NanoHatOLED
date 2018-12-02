## **NanoHat OLED**

Example code of correct use and start for the NanoHat OLED.  

Designed specifically to work with the NanoHat OLED:
http://wiki.friendlyarm.com/wiki/index.php/NanoHat_OLED

Currently supported boards (Plug & Play):
* NanoPi NEO
* NanoPi NEO Air
* NanoPi NEO2
* NanoPi NEO Plus2.

Also support other development board with the i2c interface (Need to manually connect).  


Installation
------------ 
Execute the following command in the Ubuntu core system:    

```
# git clone https://github.com/friendlyarm/NanoHatOLED.git
# cd NanoHatOLED
# sudo -H ./install.sh
```
The demo will automatically start at the next reboot.  

Remark by @bi7jta  
------------  
1) Start and stop OLED program manually to migrate to Pi-Star  
root@NanoPi-NEO:~# vi /root/NanoHatOLED/NanoHatOLED  
root@NanoPi-NEO:~# ps -ef |grep oled  
root       769   581  0 00:05 ?        00:00:00 sh -c cd /root/NanoHatOLED/BakeBit/Software/Python && python bakebit_nanohat_oled.py 2>&1 | tee /tmp/nanoled-python.log    
root       772   769  4 00:05 ?        00:00:09 python bakebit_nanohat_oled.py  
root       773   769  0 00:05 ?        00:00:00 tee /tmp/nanoled-python.log   
root      2250  1464  0 00:09 pts/0    00:00:00 grep --color=auto oled   
 
2) Increase USB-WiFi configuration  

## License

The MIT License (MIT)
Copyright (C) 2017 FriendlyELEC

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
