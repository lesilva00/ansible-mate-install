# Ansible mate install

This project permits install all packages that I costume use in my projects. Always that I use a new machine or when I need format my machine. The script is a role create by Ansible-Galaxy and can be exected using ansible-playbook command.

## Tasks added
* Python basic packages
* vim
* tmux
* bridge-utils
* lxc
* qemu
* kvm
* nftables
* ebtables
* virtualbox
* openvswitch-switch
* wireshark
* fish
* gns3-gui
* musescore
* docker
* virt-manager
* pycharm
* gedit
* nodejs
* htop
* atom
* bmon
* terminator
* eclipse
* android-studio
* git
* pavucontrol
* webtorrent

## Tasks to add
* java
* dnsmasq
* notes
* ubuntu-software-central

# How to run ansible script

First, you need install ansible:
```
$ sudo apt-get install software-properties-common
$ sudo apt-add-repository ppa:ansible/ansible
$ sudo apt-get update
$ sudo apt-get install ansible
```

After that, you need copy keys to machine that you will install packages:

```
$ ssh-copy-id <user>@<ip>
$ ssh <user>@<ip>
```
If you can access via ssh directly without the terminal asks for password, you are able to run ansible script.
In your machine, clone this project and edit inventory file add your IP. After this, execute ansible-playbook:

```
$ ansible-playbook -i inventory -u <user> -b --ask-sudo-pass site.yml
```
