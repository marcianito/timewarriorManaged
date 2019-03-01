# timewarriorManaged
run time warrior as a service using systemd

## dependencies ##
this assumes that you have a running instance of time warrior.
for most distributions works like this (or similar for yours):
``sudo apt-get install taskwarrior``

if not, checkout [here](https://taskwarrior.org/download/)

## usage ##

start/stop/resume scripts:
  * copy all twork*-files to ~/bin/
  * modify "MOSES" for the name of your standard running task (in twork_startup.sh)

systemd service files:
  * replace "mreich" in the filename with your username
  * replace "mreich" within each file with your username
  * copy all files to /etc/systemd/system/
  * start and test service: ``sudo systemctl start twarrior*@USER.service``
  * enable system service: ``sudo systemctl enable twarrior*@USER.service``
  
  
