# Public Key SSH

<https://www.geekyhacker.com/2021/02/15/configure-ssh-key-based-authentication-on-raspberry-pi/>

On Host Computer

```bash
# Go to SSH folder
ls ~/.ssh

# Generate public and privat keys
ssh-keygen -t rsa

#  Enter a file in which to save the key (/Users/you/.ssh/id_algorithm): [Press enter

# > Enter passphrase (empty for no passphrase): [Type a passphrase]
# > Enter same passphrase again: [Type passphrase again]

ssh-copy-id -i ~/.ssh/raspberrypi_rsa.pub pi-username@pi-ip-address

```

open ~/.ssh/config

```bash
Host github
  HostName github.com
  User git
  IdentityFile ~/.ssh/Github
  IdentitiesOnly yes

Host pi4
  Hostname 192.168.178.77
  User pi
  IdentityFile ~/.ssh/raspberry_pi

host parrotos
  Hostname 172.16.232.128
  user larsh
  IdentityFile ~/.ssh/parrotos
```


## Activate SSH


```bash
Type sudo apt-get install openssh-server
sudo systemctl enable ssh
sudo systemctl start ssh
