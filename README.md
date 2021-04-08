# weather-timer service
ACIT 2420 Week 11 Lab Assignment

## requirements

Linux distro that uses systemd

## installation instructions

### clone repo 

clone the repo to an appropriate location on your system

### add executable permission to script

 'chmod +x wthr'

### edit service and timer file path names
open service file in your favorite editor and edit the *ExecStart* and *WorkingDirectory* paths
Change paths to location where wthr script is installed and location where weather.txt file will be written to.

### mv service and timer

mv or copy the timer and service file to */etc/systemd/system*

 'sudo cp weather.timer weather.service /etc/systemd/system'

### reload systemd daemon list

'sudo systemctl daemon-reload'

### enable and start the timer

enable the timer so the service is run hourly *--now* option starts the timer immediately

 'sudo systemctl enable --now weather.timer'


