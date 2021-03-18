# Suit up with ansible

Ansible playbook to configure the basics of my computers

## Overview

This is my *personal* repository to have the configuration for the computers I have at hand and ready to prepare any computer, without having to downloading, installing, configuring and customizing the "basic stuff".

Feel free to use it if it suits or needs (all user-sensitive values are stored in the group_vars folders, and everything there is just a template to help), or improve it as you want. Don't forget to send a message to me, I'd love to check the new ideas!

## How to use it

You need one computer with Ansible installed (it can be the same computer you want to apply the playbook).

This computer needs to have network access to the target computer.

You need to have root access to the target computer (shared SSH keys or the root password)

Create the configuration files in group_vars:
- TODO

Run the following command:

```
ansible-playbook ROLE.yml -kK -i TARGET_HOST,
```

where
`TARGETHOST` is the IP or hostname of the target computer;
`ROLE` is the name of the role (the folder inside roles/).

## Not sure if this is what you want?

Try it in a virtual machine! I recommend installing Virtualbox, then create a VM with Ubuntu x64, configure network access, install the SSH server (`sudo apt install openssh-server`) and try to run the script.

## Two scenarios

I have two scenarios I need to cover: Raspberry Pi and Ubuntu Linux. You may need to adapt them for your needs (e.g., you use Gentoo or RHEL, or you just don't like I configure Vi). Be sure to review the steps in the playbooks and chenge them as you see fit.

## About the name

**Suit up!** was a common phrase from How I Met Your Mother's character Barney, whenever he wanted to get ready (usually, to dress a suit for some event).