# Scripts

## Today 14 Sep 2020

```
ping -c 1 192.168.1.254
ping -c 1 192.168.1.254 > ip.txt
cat ip.txt # Output should be the same as step 1
```
### Ping Sweeper

```
cat ip.txt | grep "64 bytes"
cat ip.txt | grep "64 bytes" | cut -d " " -f 4
cat ip.txt | grep "64 bytes" | cut -d " " -f 4 | tr -d ":"

nano ipsweep.sh

    #!/bin/bash

    for ip in `seq 1 254` ; do
    ping -c 1 $1.$ip | grep "64 bytes" | cut -d " " -f 4 | tr -d ":" &
    done

chmod +x ipsweep.sh
./ipsweep.sh 192.168.1
./ipsweep.sh 192.168.1 > iplist.txt
cat iplist.txt

nano ipsweep.sh

    #!/bin/bash

    if [ "$1" == "" ]
    then
    echo "You forgot an IP address!"
    echo "Syntax: ./ipsweep.sh 192.168.1"

    else
    for ip in `seq 1 254` ; do
    ping -c 1 $1.$ip | grep "64 bytes" | cut -d " " -f 4 | tr -d ":" &
    done
    fi
```

### Nmap
```
echo 'for ip in $(cat iplist1.txt); do nmap -p 80 -T4 $ip & done' > nmap1.sh
chmod +x nmap1.sh
./nmap1.sh
```
