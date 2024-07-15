+++
title = 'sshd.service'
date = 2024-07-15T23:19:50Z
draft = false
tags = ["networking" ,"Terminal"]
+++
## SSH
To connect to a remote device using ssh.You need an ssh server started on the remote device.  

###  How do you ssh?

Two ways one is through a password the other is through an ssh key.

####  Which one do you use?
If you are big on security definately the ssh key.Passwords lowkey come through if you are lazy.

so ssh key;
1. From the terminal type ``` # ssh-keygen ``` .This prompts creation of the keys and stores it at ``` 
/.ssh/id_rsa.pub ```.
2. Copy the key to the remote server at the ``` authoried_keys ``` file. Using ssh-copy-id, ``` ssh-copy-id username@remote_server.ip```

For passwords just use the pre-configured password.

#### Connecting to a remote server
Our example remote server is  'strom-2' at 196.60.66.13  
To connect we ```# ssh strom-2@196.60.66.13 ```

Where strom-2 is the username  
and   
196.60.66.13 as the remote device's ip.

Customisation
To customize your connections, ```~/.ssh/config``` allows you to specify your options.

Common mistakes : 

1. The ssh service is not running .  
Check the status by ``` # sudo sytemctl status sshd.service ```  
Start it by running ``` # sudo systemctl start sshd.service ```
enable on boot ``` # sudo systemctl enable ssd.service ```  

2. Incorrect ip address
Check and confirm the ip address of the remote server.
Run ``` ip a ``` to verify the ip.  

3. Port configuraion
ssh could blocked from listening to it's default port 22. 
Look into ``` sudo nano /etc/ssh/sshd_config
``` to see it has not be commented out or tampered with ```

4. Among others.

ssh is a valuable tool to work on projects remotely or with machines that do not have in default have display screens.

ssh is also valuable in scripting and automation,more on this on a [ later post.](https://onewaykaranja.github.io/)
