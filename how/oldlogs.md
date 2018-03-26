## Delete old logs

    find . -mtime +360 -name "*.log" -exec ls -al {} \;

Or

    find . -mtime +360 -name "*.log" -delete