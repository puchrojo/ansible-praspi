
# Install auf Ubuntu:
https://github.com/SeafileDE/seafile-server-installer

Diese Version wird es scheint, aber nur Comunity Edition von seafile-server, die Pro lauft nicht.
Dokumentation: https://wiki.ubuntu.com/ARM/RaspberryPi
  http://www.finnie.org/2015/02/16/raspberry-pi-2-update-ubuntu-14-04-image-available/



Fragen bei seafile.com welche Version sie es für die Beta nutzen.

-------------------------------------------------------------------------
Versionen von Ubuntu auf Raspi:
Source: http://www.computerbase.de/2015-03/dreimal-ubuntu-auf-dem-raspberry-pi-2/

1. Ubuntu Snappy Core: Ofizielle, aber nicht tauchbar für seafile, es sei den Über docker
   http://www.ubuntu.com/cloud/snappy
   https://developer.ubuntu.com/en/snappy/start/raspberry-pi-2/
   List app: https://uappexplorer.com/apps?type=snappy&page=2
   old: https://github.com/x86dev/docker-seafile
   old: https://github.com/JensErat/docker-seafile
   https://github.com/makkus/docker-seafile
2. Ubuntu 14.04 Trusty Tahr, basiert auf core, kann man aber ein X installieren
   https://wiki.ubuntu.com/ARM/RaspberryPi
3. Ubuntu MATE 15.04 Beta, basiert nich auf Sanppy, sonder standard Ubuntu, inofiziell
   https://ubuntu-mate.org/raspberry-pi/


------------------------------------------------------------------------------------------

Versucht mit 2. Ubuntu 14.04 Trysty Tahr.
```
cd /data/ISOs/ubuntu-14.04-Trusty-Pi-ARM
sudo bmaptool copy --bmap 2015-04-06-ubuntu-trusty.bmap 2015-04-06-ubuntu-trusty.img /dev/sdd1
```
