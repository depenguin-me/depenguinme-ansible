# Ansible recipe for depenguin.me

This is a simple ansible recipe to install FreeBSD-13.1 on a suitable host running a Linux-based rescue system.

## Pre-requisites

The server you wish to configure must be booted in the rescue console before running the playbook. 

The IP address and SSH credentials for this server need to be included in the inventory/hosts file.

## SSH Config

Make sure your .ssh/config has a setup for the host you're connecting to. 

```
Host myhost
  Hostname 1.2.3.4
  Port 22
  User username
  IdentityFile ~/.ssh/id_rsa
```

## Other variables

Edit inventory/hosts to set other variables relevant to the config. 

Do not change the SSH port assignments!

## Running

To run, edit the inventory/hosts file for your IP addresses and username, SSH keys, then run:

```
ansible-playbook -i inventory site.yml
```