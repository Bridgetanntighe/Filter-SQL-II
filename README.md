<h1>Linux | Manage Authorization  </h1>


<h2>Description</h2>
In this lab activity, I’ll use Linux commands to configure authorization.

Authorization is the concept of granting access to specific resources in a system. It's important because without authorization any user could access and modify all files belonging to other users or system files. This would certainly be a security risk.

In Linux, file and directory permissions are used to specify who has access to specific files and directories. I’ll explore file and directory permissions and change the ownership of a file and a directory to limit who can access them.

As a security analyst, setting appropriate access permissions is critical to protecting sensitive information and maintaining the overall security of a system.
<br />


<h2>Scenario </h2>
I will examine and manage the permissions on the files in the /home/researcher2/projects directory for the researcher2 user.

The researcher2 user is part of the research_team group.

I will check the permissions for all files in the directory, including any hidden files, to make sure that permissions align with the authorization that should be given. When it doesn't, I will change the permissions.


<h2>Check file and Directory details:</h2>
The lab starts with /home/researcher2 as the current working directory. This is because I'm changing permissions for files and directories belonging to the researcher2 user. <br>
1. The cd projects command navigates to the projects directory. <br>
2. The ls -l command lists the contents and permissions of the projects directory. This shows the reserch_team owns the files in the projects directory.<br>
3. The ls -la command shows whether any hidden files exist in the projects directory. This shows the .project_x.txt file is hidden. <br>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<h2>Change file permissions:</h2>
This shows whether any files have incorrect permissions and then change the permissions as needed. This action will remove unauthorized access and strengthen security on the system. <br>
1. Check whether any files in the projects directory have written permissions for the owner type with the ls -l command. This shows the project_k.txt file has write permissions for other users. <br>
2. I will change the permissions of the file identified in the previous step so that the owener type of other doesn't have write permissions. I have used the chmod command for this. <br>
(*)note - Permissions are granted for three different types of owners, namely user, group and other.(*) <br>
3. The file project_m.txt is a restricted file and should not be readable or writable by the group or other; only the user should have these permissions on this file. The ls -l command lists the contents and permissions of the current directory and check if the group has read or write permissions. This shows the group permissions of the project_m.txt file is read only. <br>
4. Using the chmod command changes permissions of the project_m.txt file so that the group doesn’t have read or write permissions. <br>

<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<h2>Change file permissions on a hidden file:</h2>
Next I will determine if a hidden file has incorrect permissions and then change the permissions as needed. This action will further remove unauthorized access and strengthen security on the system.<br>
The file .project_x.txt is a hidden file that has been archived and should not be written to by anyone. (The user and group should still be able to read this file.) <br>
1. Check the permissions of the hidden file .project_x.txt and answer the question that follows. The command to complete this step is ls -la. This shows the user and owner types have inncorrect write permissions. <br>
2. I will change the permissions of the file .project_x.txt so that both the user and the group can read, but not write to, the file using the chmod u-w,g-w,g+r .project_x.txt <br>
note - Always start the name of a hidden file with a period (.) <br>

<h2>Change directory permissions</h2>
Finally, I will change the permissions of a directory. First, I'll check the group permissions of the /home/researcher2/projects/drafts directory and then modify the permissions as required. (It's important to be in the projects directory while managing the permissions of its subdirectory drafts.) <br>
Only the researcher2 user should be allowed to access the drafts directory and its contents. (This means that only researcher2 should have execute privileges.) <br>
1. I will check the permissions of the drafts directory and answer the following question using the ls -l command. It shows the group has execute permissions and therefore has access to the drafts directory. <br>
2. I will remove the execute permission for the group from the drafts directory with the chmod command.<br>

<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<h2>Conclusion </h2>
This demonstates practical experience using basic Linux Bash shell commands to

- examine file and directory permissions, <br>
- change permissions on files, and<br>
- change permissions on directories.
