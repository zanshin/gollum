## Show 10 largest directories at top level, with total, in MB

    du -cms .[^.]*/*/ | sort -rn | head 