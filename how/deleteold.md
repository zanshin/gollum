## Delete all files older than 10 days

    find . -mtime +10 -exec rm \{} \;