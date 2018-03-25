## Find all files larger than a size, and display their human readable sizes

In this case, any file larger than 100MB

    find / -size +100MB -exec du -h {} \;