# Ansible recipe for depenguin.me

This is an ansible recipe to install FreeBSD-14.0 on a suitable host running a Linux-based rescue system.

## Prepare

The server you wish to configure must be booted into the rescue console before running this playbook from your own computer.

Note your host's IP addresses and gateway. 

Make sure your SSH public key is accessible via a URL! e.g. `http://host.tld/path/to/key.pub` 

## Update inventory file

The hostname, IP address of destination server, interface name, and your SSH public key URL, must to be set in the 
`inventory/hosts` file.

For four disk systems use `raid10` or `raidz1` instead of `mirror`. 

See comments for other optional edits.

Do not change the SSH port assignments!

## Create a python virtual environment

Do this if you want your `ansible` version to match the one tested in the repo.

Create a python virtual environment as follows:

```
python3 -m pip install virtualenv
python3 -m venv .venv
source .venv/bin/activate
(.venv) .venv/bin/python3 -m pip install --upgrade pip
(.venv) .venv/bin/python3 -m pip install -r requirements.txt
```

## Running playbooks

Make sure server is rescue mode, then from your computer run:

```
ansible-playbook site.yml
```

Or if using a virtual environment:

```
(.venv) .venv/bin/ansible-playbook site.yml
```

## Tested

Tested on:
* Hetzner AX41 (2023-03-19)
* Hetzner Server Bidding: Intel Xeon E3-1275V6 (2023-12-21)
* Hetzner EX44 (2024-05-04)
