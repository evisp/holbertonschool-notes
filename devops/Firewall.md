# Firewalls

## What is a firewall?

- In computing, a firewall is a network security system that monitors and controls incoming and outgoing network traffic based on predetermined security rules
- A firewall typically establishes a barrier between a trusted network and an untrusted network, such as the Internet

## Types of firewall

- Firewalls are categorized as a network-based or a host-based system.
- Network-based firewalls can be positioned anywhere within a LAN or WAN.
- Host-based firewalls are deployed directly on the host itself to control network traffic or other computing resources.
- This can be a daemon or service as a part of the operating system or an agent application for protection

## Packet filter

- The first reported type of network firewall is called a packet filter, which inspect packets transferred between computers.
- The firewall maintains an access control list which dictates what packets will be looked at and what action should be applied, if any, with the default action set to silent discard.
- Three basic actions regarding the packet consist of a silent discard, discard with Internet Control Message Protocol or TCP reset response to the sender, and forward to the next hop

## Install the `ufw` firewall

More details on [this tutorial](https://adamtheautomator.com/ufw-firewall/#:~:text=Install%20UFW%20first%20with%20the,to%20allow%20connections%20over%20IPv6.&text=1.,update%20for%20less%20user%20intervention.)

Even though UFW comes packaged with your Ubuntu system, UFW is not installed by default. Install UFW first with the apt package manager and configure it to allow connections over IPv6

### Update the local packages and install `uwf`

- Run on your terminal `sudo apt update -y`
- Install `uwf` on your system: `sudo apt install ufw -y`

### Configure `uwf`

- Open the UFW configuration file (`/etc/default/ufw`)
- Scroll down to the IPV6 variable and set the value to yes

### Disable and enable `ufw`

- Run the command: `sudo ufw disable && sudo ufw enable`

### Configuring Default Policies for Firewall Rules

- It’s recommended to set up a default policy for your rules
- Set up UFW to deny all incoming connections and allow all outgoing connections.
- Run: `sudo ufw default deny incoming`
- Run: `sudo ufw default allow outgoing`

### Allowing SSH Connections on the UFW Firewall

- Allowing SSH connection on your UFW firewall will do the trick to allow specific traffic in and out.
- You’ll set up an SSH server that allows incoming SSH connections on port 22
- Run: `sudo ufw allow ssh`
- Or, run: `sudo ufw allow 22`