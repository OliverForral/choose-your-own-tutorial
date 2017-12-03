# Setup SSH Key

## Required Steps

- [Register GitHub Account](/setup/register-github-account.md)

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
Make your way to [GitHub](https://github.com) and do the following

1. Click on your avatar on the top right
2. Click Settings
3. Click on SSH and GPG keys
4. Click on New SSH Key
5. Create a title
6. Paste the SSH Key
7. Click Add SSH Key

### Test SSH Connection

```bash
$ ssh -T git@github.com
```

## Next Steps

- [Install Git](/setup/install-git.md)

## Back To The Beginning

- [Start Over](/README.md)

