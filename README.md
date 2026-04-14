Test to check-out the new Raspberry reamote deploy thing:
https://www.raspberrypi.com/news/new-remote-updates-on-raspberry-pi-connect/

Artefact ffplaymp3.tar.zst
In my first example the script should do this:
#!/bin/sh
export DEBIAN_FRONTEND=noninteractive
ffplay -autoexit -nodisp -loglevel quiet '/home/mike/Music/Bobby Darin/Bobby Darin - Dream Lover.mp3'
echo Music complete
exit 0 # EXIT_SUCCESS

No errors in journalctl -t rpi-ota-connector but no sound output on the pipewire snapclient from snapserver.

Artefact pushover.tar.zst
Sends a message to the Pushover service: https://pushover.net/
Works. Useful for checking speed of deployment as the app rings on the phone when message recieved.

Artefact pyplaymp3.tar.zst
Play a mp3 form python using pygames module. This is to see if we get any sound out as ffplaymp3 didn't.
First attempt sound out from RPi audio jack with some python errors in the journalctl. Solved them by creating /etc/asound.conf and finding some stuff to ensute paths correct. Eventually deployment worked but still sound out of audio jack and not the pipe /tmp/snapfifo.

 
