# Secure Shell (SSH)

## What is a Physical Server

- A server is a piece of computer hardware or software that provides functionality for other programs or devices, called "clients".

## SSH Essentials

(Read [this](https://www.digitalocean.com/community/tutorials/ssh-essentials-working-with-ssh-servers-clients-and-keys) tutorial for more information)

- SSH is a secure protocol used as the primary means of connecting to Linux servers remotely. It provides a text-based interface by spawning a remote shell.
- After connecting, all commands you type in your local terminal are sent to the remote server and executed there.
- The SSH connection is implemented using a client-server model. This means that for an SSH connection to be established, the remote machine must be running a piece of software called an SSH daemon
- The user’s computer must have an SSH client

### How to Authenticate Users

- Clients generally authenticate either using passwords (less secure and not recommended) or SSH keys, which are very secure.
- SSH keys are a matching set of cryptographic keys which can be used for authentication. Each set contains a public and a private key. The public key can be shared freely without concern, while the private key must be vigilantly guarded and never exposed to anyone.
- To authenticate using SSH keys, a user must have an SSH key pair on their local computer. On the remote server, the public key must be copied to a file within the user’s home directory at `~/.ssh/authorized_keys`. This file contains a list of public keys, one-per-line, that are authorized to log into this account.
- When a client connects to the host, wishing to use SSH key authentication, it will inform the server of this intent and will tell the server which public key to use.
- The server then checks its authorized_keys file for the public key, generates a random string, and encrypts it using the public key. This encrypted message can only be decrypted with the associated private key.

### Generating and Working with SSH

- To generate an RSA key pair on your local computer, type: `ssh-keygen`

### Copying your Public SSH Key to a Server with SSH-Copy-ID

- To copy your public key to a server you can easily transfer your public key by typing `ssh-copy-id username@remote_host`

### Connecting to a Remote Server

- To connect to a remote server and open a shell session there, you can use the ssh command.
  - `ssh remote_host` if username on your local machine is the same as that on the remote server
  - `ssh username@remote_host` If your username is different on the remote server

## SSH Configuration File

(for detailed information refere to [this](https://www.ssh.com/academy/ssh/config) tutorial)

- The ssh program on a host receives its configuration from either the command line
or from configuration files `~/.ssh/config` and `/etc/ssh/ssh_config`.

### Commonly used configuration options

- In practice, only a few configuration options are ever changed. In most cases, just `/etc/ssh/ssh_config` is edited.

### Enabling X11 forwarding and agent forwarding

- These allow running graphical applications remotely and eliminate the need for typing a password whenever moving from one server to another, respectively. Setting these options in `/etc/ssh/ssh_config` makes life easier for end users
- `ForwardAgent yes ForwardX11 yes`

### Port forwarding

- Details are provided [here](https://www.ssh.com/ssh/tunneling/example)

### Configuring public key authentication

- Details are provided [here](https://www.ssh.com/ssh/public-key-authentication)

