# Ansible Playbook to Install the Cowrie Honeypot on Beaglebone Black

## Prerequisites

Tested with bone-debian-8.6-lxqt-4gb-armhf-2016-11-06-4gb.img booted off the SD card.

Edit the hosts file with the IP of your Beaglebone Black


## Verify Connectivity

    ansible bone -u debian -k -i hosts -m ping

## Run Playbook to Install Cowrie

    ansible-playbook -k -i hosts cowrie.yml

## Change the Root and Debian Passwords

    ssh debian@YOUR_IP

    sudo /bin/bash

    passwd root

    passwd debian

    exit

## Run cowrie

    sudo -i -u cowrie

    . ./env/bin/activate 

    cd cowrie

    ./start.sh
