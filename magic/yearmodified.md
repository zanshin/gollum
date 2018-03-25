## Find all files last modified in a particular year.

In this case, use the year 2013

    find . -printf "%TY %p\n" | grep ^2013