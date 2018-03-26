## Replace one sting with another in all files in current directory

Non-recursive, files in this directory only:

    sed -i 's/foo/bar/' *

On macOS (OS X) all `-e`, e.g., `sed -i -e 's/foo/bar/' *`

Recursively, files in this and all sub-directories

    find . -type f -exec sed -i 's/foo/bar/' {} +

Same macOS caveat for `-e` as above

from: http://unix.stackexchange.com/questions/112023/how-can-i-replace-a-string-in-a-files
and: http://stackoverflow.com/questions/19456518/invalid-command-code-despite-escaping-periods-using-sed

Alternatively,

    sed -i [-e] ’s/original/new/g’ file.txt

* `sed` - Stream EDitor  
* `-i` - in place, i.e., save to original file  
* `[-e]` - optional for macOS and OS X  
* `original` - regex or pattern to match  
* `new` - text to replace matches with  
* `g` - global  
* `file.txt` - file to operation against  
