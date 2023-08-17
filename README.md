# USERS AND GROUPS

## CREATING USERS

To create users you use the 'useradd' comfort. For example

![alt](/screenshots/useradd.jpg)

## SET AN EXPIRY DATE FOR THE USER SUCH THAT IT EXPIRES 2 WEEKS UPON CREATION

![alt](/screenshots/expiry.jpg)

In the example above, we set expiry for the user comfort we created earlier. The -e option sets expiration date for the user in format year-month-date.

## PROMPT USER TO CHANGE PASSWORD ON LOGIN

![alt](/screenshots/prompt.jpg)

The chage command provides various options for managing users such as password expiration, inactivity periods. You can use man chage to learn more.

The -d option sets the last password change date and by setting it to 0 you indicate that he password wad last changed on the day of creation.

## ATTACH THE USER TO A GROUP

To attach a user to a group, you have to first create a group.

![alt](/screenshots/group.jpg)

Here we simply just created a group named altschool using the groupadd command.

Now to attach the user to the group we do this;

![alt](/screenshots/add.jpg)

In the example above we added the user comfort we created earlier to the group altschool using usermod -aG command.

### ALLOW GROUP TO BE ABLE TO RUN ONLY cat COMMAND ON /etc/

Allowing users to run only cat command is like setting their file permissions to only read files. They cannot execute any other commands or operations on the system.

The fist step is to open the sudoers file

![alt](/screenshots/sudo.jpg)

This command above opens visudo(sudoers file).

![alt](/screenshots/cat.jpg)

In the image above the % is a sysmbol for group and altschool is the name of the group.

## CREATE A USER WITHOUT A HOME DIRECTORY

TO create a user without a home directory, you can use the useradd command with the -M option.

![alt](/screenshots/diresctory.jpg)
