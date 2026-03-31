# Update OS on the Server

This is a vital step in order to make sure that the system is up to date with the latest OS udpates. 

## Objectives

Update the packages, upgrada and verify the results.

## Steps and commands used

1.  sudo apt update - used to update the packages that can be upgraded 

![aptUpdate](https://github.com/user-attachments/assets/d437802b-197c-47af-80fc-48c120a573a4)

2. sudo apt upgrade - used to upgrade the updated packages

![aptUpgrade](https://github.com/user-attachments/assets/3e92d993-c917-4318-828d-2997a6ee67ec)

## Verification

1. apt list --upgradable - command used to see if there are others upgradable packages

![aptUpgradable](https://github.com/user-attachments/assets/f91277c8-ea81-4d76-bc68-c32782dd9332)

2. apt policy fwupd libfwupd2 - used to check why 2 packages were not upgraded.

![aptPolicy](https://github.com/user-attachments/assets/d76cd52c-5004-4acd-b557-0652400f3bd6)

The 2 packages are on "phase 20%", so the update was not yet rolled for all the systems. 

10 packages were successfully upgraded after running 'apt upgrade'.

## System Status after Upgrade

1. uname -a = used to check the system informantion

![uname](https://github.com/user-attachments/assets/b289b8da-d9c6-4540-9c81-e6d48f993ca4)

2. uptime = used to check the running time of the system

![uptime](https://github.com/user-attachments/assets/bbe0453c-355c-484e-b5a5-f03ba811835b)
