# SSH Configuration for easy access to the server

I will set SSH connection for controlling server remotely, for managing infrastructure and for transferring files.


1. sudo apt update + sudo apt install openssh-server
2. sudo systemctl status ssh - to check the ssh status

![sshcheck](https://github.com/user-attachments/assets/1543345a-9d38-407e-a849-04dd231af367)

3. From the screenshot we see that the service is installed but dead(inactive)

4. sudo systemctl start ssh - to start the service

![sshstarted](https://github.com/user-attachments/assets/d2ecd9d4-eb21-4571-af7b-24557e3e157d)


Issue happened: 

1. despite the ssh being enabled, connecting using the shell is receving a timeout

What I did:
- ping 192.xx.xx.xx - pinged the VM from windows shell to check the discoverability
- sudo ss -tulpn | grep :22 - checked if the ssh listen to port 22 (standard port for ssh)
- sudo ufw status + sudo ufw allow ssh - checked the firewall status and allowed ssh in firewall

Results: 

- SSH connection established between the server and Windows.

Issue:
- After reboot, SSH using the expected IP address no longer worked because the server received a different IP address from DHCP.

Resolution:
- Configure a static IP address using Netplan.

Steps:
- Edit the Netplan configuration:
  sudo nano /etc/netplan/50-cloud-init.yaml

- Set:
    dhcp4: false
    addresses:
      - 192.xx.xx.xx/24
    routes:
      - to: default
        via: 192.xx.xx.xx
    nameservers:
      addresses:
        - 8.8.8.8

- Apply the configuration:
  sudo netplan apply
