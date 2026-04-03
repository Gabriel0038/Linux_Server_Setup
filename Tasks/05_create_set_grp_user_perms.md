# Create and Set permissions for the groups and users

## Objectives

2 groups and 3 users should be created, one super user with all permissions and 2 other users only with write and read permissions. 

This tasks will be break in sub-tasks.

## Sub-Tasks

1. Create 2 groups:
   - developers
   - devlead
3. Create 3 users:
   - dev1 & dev2
   - devTL1
4. Assign dev1 & dev2 to develpers / assign devTL to devlead
5. Verify above steps
6. Create a working director
7. Create executable script for further permissions test
8. Set director owneship - owner: devTL / group owner: developers
9. Set director permissions:
   - Owner: devTL -> rwx
   - Group: developers -> rw-
   - Others -> ---
11. Create colaborative folder:
    - all users can write; new files assigned to developers via setgid
12. Test each user permissions

## Sub-Task Progress

1. 
