## Delete Specific Line in Any File

### Deletes line 147 from .ssh/known_hosts

    vim .ssh/known_hosts +”147d|x” 

### Deletes lines 147 & 145 from .ssh/known_hosts

    sed -I .bak -e 147d -e 145d .ssh/known_hosts