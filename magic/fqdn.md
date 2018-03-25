## Show FQDN on SunOS

    uname -n | xargs nslookup | grep Name | awk {'print $2'}