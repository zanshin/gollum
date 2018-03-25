## Show IPv4 and IPv6 addresses per interface

    echo show|ip -o -b -|cut -d' ' -f2,7