## Quickly scan the network, without using `nmap`

    for i in 192.168.1.{1..254} ; do (ping -c1 $i > /dev/null && echo $_)&done > pinged-hosts