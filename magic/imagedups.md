## Find any duplicate images in a directory

In this case, only `JPG` images

    shasum *.jpg | awk {'print $1'} | sort | uniq -c | grep -v " 1 "