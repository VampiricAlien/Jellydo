<h1>Jellyfin Frequently Ask Questions</h1>
  
<stong>Jellyfin webpage not displaying how it should?</strong>
Clear browser cache and reload the page.

<strong>Jellyfin web not working after upgrading to 10.7.0</strong>
Reinstall jellyfin-web (/usr/share/jellyfin/web). OR replace the config file and add the contents from <a href="https://github.com/jellyfin/jellyfin-web/blob/master/src/config.json">

<strong>Jellyfin can't read my media</strong>
Command line (terminal): sudo chown -R jellyfin /media/yourusername/mediadrive (eg: sudo chown -R jellyfin /media/VampiricAlien/jellyfinmedia).

<strong>What video files does Jellyfin support?</strong>
<a href="https://jellyfin.org/docs/general/clients/codec-support.html">

<strong>What is the best Video Compatibility file to use?</strong>
MP4 as more clients support this.

<strong>Best video codec to use?</strong>
H.264 (AVC) 8Bit - this codec is supported by all jellyfin clients and all browsers (Direct play)

<strong>Where are the logs?</strong>
http://xxx.xxx.xxx.xxx:8096/web/index.html#!/log.html (x = IP address) You can also find the logs in /var/log/jellyfin

<strong>Saving Artwork into media folders</strong>
Each library has it's own settings, you can find them by going into the admin dashboard then library then the 3 dotted menu to edit the library.

<strong>Working with reverse proxy</strong>
https://jellyfin.org/docs/general/networking/index.html

<strong>Can't connect to my server after installing a VPN</strong>
VPN settings should have an option for access to LAN.

<strong>Locked out of admin account</strong>
Edit the jellyfin.db. From the command line install sqlite3 (database editor) sudo apt install sqlite3 then once intalled sudo -u jellyfin sqlite3 /var/lib/jellyfin/data/jellyfin.db

<strong>How do I backup Jellyfin?</strong>
Copy everything from /var/lib/jellyfin 
Using Docker: For binds: you back up the folder you’ve set for config. 
For volumes: follow the instructions at https://docs.docker.com/storage/volumes/#backup-restore-or-migrate-data-volumes for the volume holding the config.
