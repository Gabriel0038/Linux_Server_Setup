# New hostname to be set for the server

## Objective

Set a custom hostname for the server.

## Commands used

1. cat /etc/hostname - used to check the current hostname

![cat/etc/hostname](https://github.com/user-attachments/assets/917d104f-1e93-46f0-9918-4b56a7b2f864)

2. sudo hostnamectl set-hostname project-server - used to modify the hostname

3. cat /etc/hostname or hostnamectl commands to check the results

## Results 

![results](https://github.com/user-attachments/assets/46ac6a9a-ded0-4b64-8482-94dda8b950fd)

## Map the IP address to the hostname in /etc/hosts

1. sudo nano /etc/hosts - used to edit the /etc/hosts file - added "127.0.1.1 project-server" & write the file

![/etc/hosts](https://github.com/user-attachments/assets/1c6ceebb-2766-4635-9f0a-e307659f4b40)
