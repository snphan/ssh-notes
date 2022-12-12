# Some Notes When Setting up SSH

# SSH Commands

# How to SSH
To ssh into another computer use the following command

    ssh -p <port> <username>@<hostname>
  
If you have the ~/.ssh/config setup, then you can 

    ssh <host alias>
  

# How to copy

    scp <file name on server> <username>@<hostname>:/path/to/file
  
# How to setup key-pair

On the client make a key. There are some parameters that you can add to make it more secure. Google this.

    ssh-keygen 
    
Copy the key to the server

    ssh-copy-id -i ~/.ssh/mykey user@host
    
Disable password login in the server because password login is a security risk!

# ~/.ssh/config

1. This is where the alias for your hosts are stored
```
Host <host alias>
    HostName <host ip address>
    Port <port number>
    IdentityFile ~/.ssh/id_rsa.pub
    User <username>
```

# WSL

1. Use WSL1, WSL2 is a hassle to setup.

Need a way to sudo service ssh start on boot...
