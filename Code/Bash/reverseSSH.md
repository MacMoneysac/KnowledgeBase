# Reverse SSH

## How does it work

Reverse SSH tunneling allows you to use that established connection to set up a new connection from your local computer back to the remote computer.

Because the original connection came from the remote computer to you, using it to go in the other direction is using it “in reverse.” And because SSH is secure, you’re putting a secure connection inside an existing secure connection. This means your connection to the remote computer acts as a private tunnel inside the original connection.

Remote Computer ---[Hey, please talk with me]---> Local Computer with static IP

Remote Computer <---[Okay, here we go]--- Local Computer with static IP (one the same console)

## Installation on Remote Computer

wenn kein direkt SSH möglich ist (google cloud) dann zunächst public key SSH einrichten

```bash
ssh -R 25565:localhost:22 dave@sulaco.local
```

jupiter: 34.159.121.230

- The -R (reverse) option tells ssh that new SSH sessions must be created on the remote computer.
- The “43022:localhost:22” tells ssh that connection requests to port 43022 on the local computer should be forwarded to port 22 on the remote computer. Port 43022 was chosen because it is listed as being unallocated. It isn’t a special number.
- dave@sulaco.local is the user account the remote computer is going to connect to on the local computer.

On Remote Computer connected to Local Computer

```bash
ssh localhost -p 25565
```

## AutoSSH Installation

Sounds like you need autossh. This will monitor an ssh tunnel and restart it as needed. We've used it for a couple of years and it seems to work well.

apt install autossh

```bash
autossh -M 20000 -f -N jupiter -R 25565:localhost:22 -C

# in /etc/crontab
@reboot pi autossh -M 20000 -f -N jupiter -R 25565:localhost:22 -C
```

## Ports

pi4: 25565
pi3: 25566
