# Install Git

## Required Steps

- [Register Gmail Account](/setup/register-gmail-account.md)

## Setup

### Use Apt

```bash
$ sudo apt install git
```

### Configure Vim

```bash
$ vi ~/.vimrc
set backspace=indent,eol,start
set nocompatible
```

### Configure Git

```bash
$ vi ~/.gitconfig
[user]
        name = Your Name
        email = your_email@example.com
[core]
        editor = /usr/bin/vi
        whitespace = cr-at-eol
[color]
        ui = true
[push]
        default = simple

```

## Next Steps

- [Install Docker](/setup/install-docker.md)

## Back To The Beginning

- [Start Over](/README.md)

