# Create and Set permissions for the groups and users

## Objectives

2 groups and 3 users should be created, one super user with all permissions and 2 other users only with write and read permissions. 

This tasks will be break in sub-tasks.

## Sub-Tasks

1. Create 2 groups: developers & devlead
2. Create 3 users: dev1 & dev2 & devTL1
3. Assign dev1 & dev2 to develpers / assign devTL to devlead
4. Verify above steps
5. Create a working director
6. Create executable script for further permissions test
7. Set director owneship - owner: devTL / group owner: developers
8. Set director permissions:
   Owner: devTL -> rwx
   Group: developers -> rw-
   Others -> ---
9. Create colaborative folder:
    - all users can write; new files assigned to developers via setgid
10. Test each user permissions

## Sub-Task Progress

1. 
