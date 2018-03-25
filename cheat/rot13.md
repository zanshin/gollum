## ROT13

Encryption:  
    echo 'This is a Test' | tr 'A-Za-z' 'N-ZA-Mn-za-m'

Output: Guvf vf n Grfg

Decryption:  
    echo 'Guvf vf n Grfg' | tr 'A-Za-z' 'N-ZA-Mn-za-m'

Output: This is a Test