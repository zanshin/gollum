## Find space used

    du -kx > /tmp/du.out
    cat /tmp/du.out | sort -nr | less