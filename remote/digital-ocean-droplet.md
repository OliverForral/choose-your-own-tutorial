# Digital Ocean Droplet

## Required Steps

- [Setup SSH Key](/setup/setup-ssh-key.md)
- [Register Digital Ocean Account](/setup/register-digital-ocean-account.md)

## Setup

### Add SSH Key

Make your way to [Digital Ocean](https://www.digitalocean.com/) and do the following:

1. Click on your avatar
2. Click on `Settings`
3. Click on `Security`
4. Click on `Add SSH Key`
5. Fill out `SSH key content` and `Name`
6. Click on `Add SSH Key`

### Create Droplet

1. Click on the `Create` dropdown
2. Click on `Droplets
3. Under `Choose a size`, click on `$5/mo`
4. Under `Choose a datacenter region`, under `San Francisco`, click on `2`
5. Click on `Create`
6. Wait for it to finish creating
7. Next to the IP Address, click on `Copy`

### Setup Droplet

If the IP address was 1.2.3.4

```bash
$ ssh root@1.2.3.4
```

## Next Steps

none yet

## Or none of these?

- [Start Over](/README.md)
