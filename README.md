# Ansible recipe for depenguin.me

This is an ansible recipe to install FreeBSD-13.2 on a suitable host running a Linux-based rescue system.

## Prepare

The server you wish to configure must be booted in the rescue console before running the playbook. 

Note your host's IP addresses and gateway.

Make sure your SSH public key is accessible via a URL! e.g. `http://host.tld/path/to/key.pub` 

## Update inventory file

The hostname, IP address of destination server, and your SSH public key URL, must to be set in the `inventory/hosts` file.

See comments for other optional edits.

Do not change the SSH port assignments!

## Running playbooks

Make sure server is rescue mode, then from your computer run:

```
ansible-playbook site.yml
```

## Tested

Tested on:
* Hetzner AX41 (2023-03-19)