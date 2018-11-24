# alexa-autostart-boot
Run Amazon Alexa automatically on boot on Raspberry Pi easily.

## Install screen

  **sudo apt-get install screen**

## Add these lines to he end of /etc/profile file

  **screen -dmS "alexa"**
  
  **screen  -S "alexa" -X stuff "sudo bash startsample.sh ^M"**

Create a detached screen in the first line and then send command to run the startsample to the detached screen. 

Note: The profile file gets executed twice, hence you see two screens on boot, however the alexa app run on the first one. 

## To see the screen in which alexa is running

  **screen -r <screen id>**
  
### You can get screen id using
  **screen -ls**
  
  
  
Referece: https://unix.stackexchange.com/questions/13953/sending-text-input-to-a-detached-screen
