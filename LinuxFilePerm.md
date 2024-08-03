# File permissions in Linux

## Project description

The research team at my organization needs to update the file permissions for certain files and directories within the projects directory. The permissions do not currently reflect the level of authorization that should be given. Checking and updating these permissions will help keep their system secure. To complete this task, I performed the following tasks:

### Check file and directory details
```
ls -la
```
I used the ls command with the -la option to display a detailed list of the file contents. The output contains a 10 character string that represents  the permissions set for each file in the directory. 

### Describe the permissions string

The 10-character string can be deconstructed to determine who is authorized to access the file and their specific permissions. 

1st character: This character is either a d or hyphen (-) and indicates the file type. If it’s a d, it’s a directory. If it’s a hyphen (-), it’s a regular file.

2nd-4th characters: These characters indicate the read (r), write (w), and execute (x) permissions for the user. When one of these characters is a hyphen (-) instead, it indicates that this permission is not granted to the user.

5th-7th characters: These characters indicate the read (r), write (w), and execute (x) permissions for the group. When one of these characters is a hyphen (-) instead, it indicates that this permission is not granted for the group.

8th-10th characters: These characters indicate the read (r), write (w), and execute (x) permissions for other. This owner type consists of all other users on the system apart from the user and the group. When one of these characters is a hyphen (-) instead, that indicates that this permission is not granted for other.

### Change file permissions

I determined that a project must have the write access removed for other. I used the following command to do so: 
```
chmod o-w project.txt
```
The chmod command changes the file permissions on files and directories. The first argument indicates that the other permissions should be modified and the second argument indicates that the write permission should be removed. 

### Change file permissions on a hidden file

The research team recently archived a file that they do not want anyone to have write access to, but user and group should have read access. 

I used the following code to do so:
```
chmod u-w,g-w,g+r .project.txt
```
The (.) indicates that the project is a hidden file. I removed write permissions from user and group, and added read permission to group, as user already had read permission. 

### Change directory permissions

My organization only wants the researcher2 user to have access to the drafts directory and its contents. This means that no one other than researcher2 should have execute permissions.

I used the following code to do so: 
```
chmod g-x drafts 
```
Researcher2 already has execute permissions so I do not have to add them. I removed the group execute permissions. 


