# SSH Configuration for easy access to the server

I will set SSH connection for controlling server remotely, for managing infrastructure and for transferring files.


1. sudo apt update + sudo apt install openssh-server
2. sudo systemctl status ssh - to check the ssh status

![sshcheck](https://github.com/user-attachments/assets/1543345a-9d38-407e-a849-04dd231af367)

3. From the screenshot we see that the service is installed but dead(inactive)

4. sudo systemctl start ssh - to start the service

![sshstarted](https://github.com/user-attachments/assets/d2ecd9d4-eb21-4571-af7b-24557e3e157d)
