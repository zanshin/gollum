## Parse a http log for top hits

    grep "18/Sep/2014:03" blogs.k-state.edu.ssl.xfer.log | awk '{print $1}' | sort -n | uniq -c | sort -nr | head -20