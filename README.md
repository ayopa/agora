# How to build

First of all install eta

    git clone https://github.com/ayopa/eta.git
    cd eta
    makepkg -i

Then build the agora packages

    git clone https://github.com/ayopa/agora.git
    cd agora
    sudo eta-build

Construct the root filesystem and commit it

    sudo eta-commit

Create the OS image

    sudo eta-pack

Copy it to an USB drive

    sudo dd if=out/agora.img of=/dev/sd[X] bs=1M
