## Tail log and highlight errors

    tail -f foo.log | egrep --line-buffered --color=auto 'ERROR|WARN|$' 