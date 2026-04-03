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
3. Assign dev1 & dev2 to develpers / assign devTL to devlead
4. Verify above steps
5. Create a working director
6. Create executable script for further permissions test
7. Set director owneship - owner: devTL / group owner: developers
8. Set director permissions:
   - Owner: devTL -> rwx
   - Group: developers -> rw-
   - Others -> ---
9. Create colaborative folder:
    - all users can write; new files assigned to developers via setgid
10. Test each user permissions

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

 
