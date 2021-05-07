Linux is a multi-user system, which means that more than one person can interact with the same system at the same time.

Users :

1) Users command in Linux system is used to show the user names of users currently logged in to the current host.
2) You can create multiple users in a Linux operating system using Linux user commands. 
3) It will display who is currently logged in according to FILE.
4) Each user identified with unique identification number.

Syntax   : user [options] ..[file]
           Users command without any option will print the users currently logged in.
Options  : –help    - This option will display the help message and exit.         
           –version - This option will show the version information and exit.
           
The steps for creating new user are :
Step 1) : Use command sudo adduser.
Step 2) : Enter te password for new account and confirm.
Step 3) : Enter the details of new user and press Y.
New account is created.

Get a List of All Users using the /etc/passwd File.

Once you enter /etc/passwd file it contains:

1) User name.
2) Adding...
3) User ID number (UID).
4) User’s group ID number (GID).
5) Full name of the user (GECOS).
6) User home directory.
7) Login shell (defaults to /bin/bash).

Groups : 

1) In Linux, a group is a collection of users.
2) The main purpose of group is to define a set of privileges like read , write or execute permission for given resources tht can be shared among the users among the group.

Syntax   : group [options]..[username]
           Print group memberships for each username, if username not provided process for the current one.
Options  : -help   - Display help and exit
           -verson - Output version information and exit.
           
There are two types of groups user can belong : 

1) Primary or Login group           : The group that are assigned to the files that are created by user. Usually name of primary group is same as the name ofof user.Each user should belong to exactly one primary group.

2) Secondary or supplementary group : used to grant certain privileges to a set of users. A user can be a member of zero or more secondary groups.

The steps for creating new group are : 

1) To create a new group type sudo groupadd followed by the new group name.
2) Once the group is created, you can start adding users to the group.
3) The sudo command will now prompt you to enter the password for your administrator account.
4) After you have entered your password, press the Enter key to continue.
5) If it goes well without any error, this indicates that group has added successfully.
6) to ensure group has added to system enter sudo tail /etc/group

Sudo User :

1) Basically sudo user is a tool that allows users & groups to have access to commands they normally would not able to access.
2) Sudo enables user to have administration privilliges without logging in directly as a root user.

The operations perfermed on groups and users are :

1)  whoami            : Used to display the username of the current use.
2)  su                : Used to switch user
3)  useradd           : Used to add a user to the system.
4)  userdel           : Used to delete a user account and related files.
5)  groupadd          : Used to add a group to the system.
6)  delgroup          : Used to remove a group from the system.
7)  groupdel          : Used to delete group
8)  usermod           : Used to modify a user account.
9)  usermod -aG admin : Used to append user to the secondary group.
10) cat /etc/passwd   : Used to check addition of the user 
11) passwd            : Used to assign the password to user  
12) id                : Used to get data about user and its group 
13) chage             : Used to change user password expiry information.
14) sudo              : Used to run one or more commands as another user typically with superuser permissions.