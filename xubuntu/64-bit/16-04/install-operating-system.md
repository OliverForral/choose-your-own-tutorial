# Install Operating System 64-bit Xubuntu 16.04

## Required Steps

There are no required steps.

## Welcome Screen

### Internet

You decide to connect to the internet.
On the top right of the screen, you click the icon that has an up arrow and a down arrow.
You type in wifi information and now the "up arrow and down arrow" icon has turned into a signal icon.

### Try Xubuntu Or Install Xubuntu

At this point, you see a "Try Xubuntu" button and a "Install Xubuntu" button.
Since you plan to install other applications, you decide to click the "Install Xubuntu" button.

### Preparing To Install Xubuntu

You now see two checkboxes
The first checkbox is for downloading updates while the operating system in installing.
The second checkbox is for installing third-party software, which may include some that are proprietary.
You decide to check both boxes and click the "Continue" button.

### Installation Type

Since there were no previously installed operating systems,
there was only one radio button for erasing the disk and installing Xubuntu.
You leave the other checkboxes clear since you do not need the extra security and you click the "Install Now" button.

### Where Are You?

You pick the city closest to the one are at and you click the "Continue" button.

### Keyboard Layout

You pick the language closest to the layout of your keyboard and you click the "Continue" button.

### Who Are You?

You type in what you think your name is and a password.
You also click the "Log in automatically" option and then click the "Continue" button.

## After Installation

### Internet Again

You notice that the internet credentials during installation were not saved.
On the top right of the screen, you click the icon that has an up arrow and a down arrow.
You type in wifi information and now the "up arrow and down arrow" icon has turned into a signal icon.
At this point, the internet isn't quite connected, so you restart the computer just to be sure.

### Terminal Emulator

You click on the top left button which opens up the main system menu.
It defaults to the favorites tab and near the bottom of the list, you click on Terminal Emulator.

### Fixing Some Known Errors

Since you are aware of issues with this installer, you decide to type this in.

```bash
sudo apt install --reinstall libappstream3
```

### Update Package Repositories

You type in the following to update your package repositories.

```bash
sudo apt-get update;
```

### Upgrade Packages

You type in the following to upgrade your packages.

```bash
sudo apt-get upgrade;
```

## Next Steps

What will you do next?

- [Register Email](/register-email.md)

Or none of these?

- [Start Over](/README.md)
