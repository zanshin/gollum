## Count the number of web server processes running

    ps -ef | grep "[h]ttpd" | wc -l

    pgrep -c httpd