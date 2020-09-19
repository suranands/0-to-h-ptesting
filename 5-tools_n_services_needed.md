# Tools & Services Needed

## Today 13 Sep 2020

- `apt install git`
- `apt install ftp`
- Now we need a tool called **impacket**, but Cyber Mentor asked us to remove (purge) completely the one that already came with this VM file. Not sure why. Maybe to show us how to install it from scratch and learn to build it ourselves.
- So you need to go to google *'impacket github'*, go to the [github page](https://github.com/SecureAuthCorp/impacket), and copy the clone [link](https://github.com/SecureAuthCorp/impacket.git). See the `readme` and install it. Quite simple, nothing to worry much.
- Then you need to start some services if they are not already running.
- `ifconfig` and get your IP add.
- Go to browser, paste your IP add, and see if default apache page is loaded. Mostly, it won't because the service is not started.
- Now run `service apache2 start`
- Go to browser and refresh the page with your IP add in the URL, this should now load the default apache page. So, all that needed to be started are...
```
service apache2 start
service ssh start
service postgresql start
```
- `Postgresql` is needed because Metasploit uses this.
- All services will be stopped once you turn off the system.
- To avoid this problem, run `systemctl enable ssh`, this ensures the system boots up with these services running.
