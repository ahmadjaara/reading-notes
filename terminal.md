# What Is command line?
Deal with command here you will write a command by tools (such as TERMINAL) to interact with your operating system 
An important part in the terminal is the shell is a part of the operating system that define how the terminal will behave and looks after running command for you
Shortcut: using up arrow to use previous command in the history 
terminal is a case sensitive for naming directory and command so file different from lower case and upper case naming , and it is also space sensitive to write a directory name has a space in its name we use \before the space or we put the directory or file name in side ‘ ’or we can use tab before the space when we write the directory or file name  
Path:
Relative path: A file or directory location relative to where we currently are in the file system. (Directory name) 
Absolute path: A file or directory location in relation to the root of the file system. /

Manual pages it is a help cheat to search for a command 
To call it 
man<command you want to look up for it>
man -k <search term search for keyword >
/<term>search inside the current manual page 
n next found item after search command

command:
pwd: (path word description) show you the path that you are working on 
Ls:(list) to show the file inside any directory  ls [options] [location]:
Ls -l: give me more details about the content of the directory (d=direc. / -=file)
ls /etc: it tells ls not to list our current directory but instead to list that directories contents.
ls -a: List the contents of a directory, including hidden files.(any hidden file or directory start with dot(.))
Cd: Change Directories - ie. move to another directory. If you run the command cd without any arguments then it will always take you back to your home directory.
file: obtain information about what type of file a file or directory is. ** Everything is a file under Linux Even directories. Linux is an extensionless system Files can have any extension they like or none at all since it look inside the file before give it a type 



file manipulation:
making a directory (mkdir [options] <Directory>)
delete a directory (rmdir [options] <Directory>)
touch: to create a file
cp: copy file you use it by write the file or directory that you want to copy after that write the name of the copy file 
mv: to move a file or directory mv then the name of file you want to move then the name of place \here if you want to change the directory or file name 
rm: to delete a file 
