# Setup SSH Key For 64-bit Xubuntu 16.04

## Required Steps

- [Install Operating System 64-bit Xubuntu 16.04](xubuntu/64-bit/16-04/install-operating-system.md)

## Setup

### Check For Existing SSH Keys

Open a terminal and enter the following

```bash
$ ls -al ~/.ssh
```

### Generate New SSH Key

```bash
$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

### Add SSH Key To SSH Agent

```bash
$ eval "$(ssh-agent -s)"
$ ssh-add ~/.ssh/id_rsa
```

### Add SSH key To GitHub Account

```bash
$ sudo apt-get install xclip
$ xclip -sel clip < ~/.ssh/id_rsa.pub
```
