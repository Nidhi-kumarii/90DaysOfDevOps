File & Directory Permissions

Task:
Create '/devops_workspace' and a file 'project_notes.txt'.
Set permissions:
Owner can edit, group can read, others have no access.
Use 'ls -l' to verify permissions.

===========================

Linux permissions control access to files and directories for users, groups, and others.

Permissions are shown using 'ls -l' as: '-rwxr-x--- 1 owner group filename' Where:

'r' = read
'w' = write
'x' = xecute

Setting permissions example:

Create directory and file:

```bash
mkdir /devops_workspace
touch /devops_workspace/project_notes.txt
```
change ownership to your user and group :

```bash

sudo chown devops_user:devops_team /devops_workspace/project_notes.txt
```
Set permissions so owner can edit, group can read, others no access :

```bash
  chmod 640 /devops_workspace/project_notes.txt
```

Verify permissions:

```bash
  ls -l /devops_workspace/project_notes.txt
```




