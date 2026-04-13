Test to check-out the new Raspberry reamote deploy thing:
https://www.raspberrypi.com/news/new-remote-updates-on-raspberry-pi-connect/

In my first example the script should do this:
#!/bin/sh
export DEBIAN_FRONTEND=noninteractive
ffplay -autoexit -nodisp -loglevel quiet '/home/mike/Music/Bobby Darin/Bobby Darin - Dream Lover.mp3'
echo Music complete
exit 0 # EXIT_SUCCESS
