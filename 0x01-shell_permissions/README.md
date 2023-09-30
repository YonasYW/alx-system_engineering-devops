su betty changes the user to betty
whoami prints effective user name
groups prints all the groups
chown betty hello changes the owner of the file "hello" to the user "betty"
touch hello creates an empty file called hello
chmod u+x hello adds execute permission to the owner of the file "hello"
chmod u+x,g+x,o+r hello adds execute permission to the owner and the group owner, and read permission to other users, for the file "hello"
chmod ugo+x hello adds execution permission to the owner, the group owner, and other users for the file "hello"
chmod 007 hello gives permission only to others
chmod 751 hello ets the mode of the file "hello" to -rwxr-x-wx
mode=$(stat -c "%a" olleh) && chmod "$mode" hello sets the mode of the file "hello" to be the same as the mode of the file "olleh" 
find . -type d -exec chmod +x {} + adds execute permission to all subdirectories of the current directory for the owner, the group owner, and all other users, while leaving regular files unchanged
mkdir my_dir && chmod 751 my_dir creates a directory called "my_dir" with permissions 751
chgrp school hello changes the group owner of the file "hello" to "school"

