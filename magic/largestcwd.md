## List the 5 largest files in the current working directory (CWD) without crossing file system boundaries

    find . -xdev -ls | sort -n -k 7 | tail -5