# Install Git On 64-bit Xubuntu 16.04

## Required Steps

- [Install Operating System 64-bit Xubuntu 16.04](/xubuntu/64-bit/16-04/install-operating-system.md)
- [Register Email](/register-email.md)

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

### Steps That Have Similar Requirements

None yet.

### Steps That Require This

None yet.

### Back To The Beginning

- [Start Over](/README.md)

