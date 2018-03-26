## Remove a package via `dpkg` and `apt`

See what :

    dpkg --get-selections | grep foo

Remove `foo`

    sudo dpkg --force-all -r foo

Autoremove to clean up

    sudo apt -y autoremove