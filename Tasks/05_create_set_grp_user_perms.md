# Create and Set permissions for the groups and users

## Objectives

2 groups and 3 users should be created, one super user with all permissions and 2 other users only with write and read permissions. 

This tasks will be break in sub-tasks.

## Sub-Tasks

1. Create 2 groups:
   - developers
   - devlead
2. Create 3 users:
   - dev1 & dev2
   - devTL1
3. Assign:
   - dev1 & dev2 to develpers
   - devTL to devlead & developers
4. Create a working director
   - workingdir to be created in /srv
5. Create executable script for further permissions test
6. Set director owneship - owner: devTL / group owner: developers
7. Set director permissions:
   - Owner: devTL -> rwx
   - Group: developers -> rw-
   - Others -> ---
8. Create colaborative folder:
    - all users can write; new files assigned to developers via setgid
9. Test each user permissions

## Sub-Task Progress

### Sub1. 

1. sudo groupadd developers & sudo groupadd devlead - used to create the groups.
2. cat /etc/group | grep dev - pipe to check that the groups were created 

![grepdev](https://github.com/user-attachments/assets/d4788fe5-fd25-4d22-bd93-cb7c2c741a25)

### Sub2. 

1. sudo useradd - used to create new users
2. cat /etc/passwd | grep dev - pipe for verification

![grepuser](https://github.com/user-attachments/assets/439d9c4c-9fef-43f6-b11d-22cee8b7eea8)

### Sub3.

1. For 3rd sub-task I have to find each ID for new groups created and assign the 3 new users to the relevant groups. 
cat /etc/group | grep dev - used again to identify group IDs. 
In this case we have the following IDs:
   - developers: ID = 1001
   - devlead: ID = 1002

2. usermod -g - used to move users under relevant groups
3. cat /etc/passwd | grep dev - to verify

![usermod](https://github.com/user-attachments/assets/c22b11be-f4d2-42c6-af7f-8d0cd31e5761)

4. As devTL1 should be in both groups => usermod -aG 1001 devTL1 - used to add the user in the developers group also. 

![devTL](https://github.com/user-attachments/assets/cd1349c1-d7f4-4f71-83d9-33ff5f597499)

### Sub4. 

- cd /srv - used to move the directory
- sudo mkdir workingdir - used to create the dir
- ls - used to verify

![mkdir](https://github.com/user-attachments/assets/7732ca5b-2150-43e9-a259-cfb490f288ba)

### Sub5.

- touch deploy.sh - used to create a file
- ls to verify it

![touchfile](https://github.com/user-attachments/assets/d4441f1a-5f9f-4e69-a24f-3ef8840f7800)

### Sub6. 



 
