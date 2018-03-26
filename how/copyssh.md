## Copy ssh key to machine that doesn't have ssh-copy installed

    cat ~/.ssh/id_rsa.pub | ssh user@machine "mkdir -p ~/.ssh; cat >> ~/.ssh/authorized_keys"