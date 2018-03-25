## List top `404` errors in descending order

    awk '$9 == "404" {print $7}' access.log | sort | uniq -c | sort -rn | head -n 50