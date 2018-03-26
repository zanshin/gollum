## Configure multiple things with the same static IP address pre-configured

# Ping the IP

2) apr -a to see the cooresponding MAC address
3) apr -s mac-address (to make sure you always are seeing the same one)
4) connect to the device and change the IP address
5) arp -d ip-address to delete your staic MAC<->IP mapping
6) Loop until done

Should work on Linux, Windows, or Mac