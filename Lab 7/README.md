# Lab 7 - ThingSpeak and Google Sheets
I pledge my honor that I have abided by the Stevnes Honor System - _Andrea Antropow_
## ThingSpeak
I already had a MathWorks account so I signed in to ThingSpeak. Then, I created a new channel called cpu_loop with fields for cpu_pc and mem_avail_mb.

Ran following code

```sh
$ sudo pip3 install -U psutil
$ cd ~/demo
$ cp ~/iot/lesson7/thingspeak_cpu_loop.py .
$ cp ~/iot/lesson7/thingspeak_feed.py .
$ cat thingspeak_cpu_loop.py
$ cat thingspeak_feed.py
$ python3 thingspeak_feed.py
An API key savefile was not found. Enter Write API Key >>>
Should we save this key for future use? [y/N] >>>
```

![image](https://github.com/user-attachments/assets/6c1f0ab8-077d-45e3-862b-e2395c9cd44c)

These were the chart outputs. 

![image](https://github.com/user-attachments/assets/530b60d6-82a6-4733-97ba-8cf6fbf95384)

## Google Sheets and API

Created a new project on Google Cloud Platform Identity and Access Management [(IAM)](https://console.developers.google.com/projectselector/iam-admin/iam)
Also created a service account key and saved the .json file. 

Next, I installed the necessary Python packages using ```pip install -U gspread oauth2client```

![image](https://github.com/user-attachments/assets/fb1e4d04-564e-4722-8e62-90f2f5022916)


Copied necessary python files to current working directory
```
cp ~/iot/lesson3/system_info.py .
cp ~/iot/lesson7/cpu_spreadsheet.py .
```
![image](https://github.com/user-attachments/assets/ab0d5f0c-429d-45ef-a12e-68661e8cef53)

Also used ```mv ~/Downloads/cpudata-xxxxxxxxxxxx.json``` to working directory. 

Created a Google Sheets file named cpudata and deleted rows 2-1000. Shared the spreadsheet with "client_email" address given in the service account key for .json file.

Needed to use ```nano cpu_spreadsheet.py``` to change it to my API information. 


Ran the ```python3 cpu_spreadsheet.py```

The Google Sheet updated very close to every 10 seconds with new data. 
![image](https://github.com/user-attachments/assets/31bd655b-da6e-45fa-a85c-c5a0323fa5af)
