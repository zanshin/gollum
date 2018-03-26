## JVM thread or process dumps

To get a dump of a running process:

    jmap -dump:format=b,file=blah.bin <pid>

The output from this is not human readable - will need MAT ([http://www.eclipse.org/mat/](http://www.eclipse.org/mat/)) or something similar to read.

To get a thread dump of a running process:

    jstack <pid>