## Rebuild physical/virtual disk layout

# Determine what virtual groups you have starting out

    sudo vgdisplay

# we don't want the /var/log/audit space so we'll get rid of it

    sudo umount /var/log/audit

# and comment it out of fstab

    printf '/audit\ns/^/#\nw\nq\n' | sudo ed /etc/fstab

# remove the logical volume and say yes to the prompt
    
    sudo lvremove /dev/newhome/home
    Do you really want to remove active logical volume home? [y/n]: y

# display the physical volumes and find the one we are interested in

    sudo pvdisplay

# remove the virtual group
  
    sudo vgremove newhome

# remove the physical group

    sudo pvremove /dev/sdd

# recreate a new physical group with the same name

    sudo pvcreate /dev/sdd

# and extend the virtual group we want to keep to use the new space

    sudo vgextend vg /dev/sdd

