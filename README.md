# Basiccommands
This is the Markdown with the basic commands.

Linux commands may seem intimidating at first glance if you are not used to using the terminal. There are many commands for performing operations and processes on your Linux system.

Basic Linux commands list.

Hardware information

dmesg -> Show bootup messages
cat /proc/cpuinfo -> See CPU information
free -h -> Display free and used memory with
lshw -> List hardware configuration information
lsblk -> See information about block devices

Searching

grep [pattern] [file_name] -> Search for a specific pattern in a file with
grep -r [pattern] [directory_name] -> Recursively search for a pattern in a directory
locate [name] -> Find all files and directories related to a particular name
find [/folder/location] -name [a] -> List names that begin with a specified character [a] in a specified location [/folder/location] by using the find command
find [/folder/location] -size [+100M] -> See files larger than a specified size [+100M] in a folder

File Commands

ls -> List files in the directory
ls -a -> List all files (shows hidden files)
pwd -> Show directory you are currently working in
mkdir [directory] -> Create a new directory
rm [file_name] -> Remove a file
rm -r [directory_name] -> Remove a directory recursively
rm -rf [directory_name] -> Recursively remove a directory without requiring confirmation
cp [file_name1] [file_name2] -> Copy the contents of one file to another file
cp -r [directory_name1] [directory_name2] -> Recursively copy the contents of one file to a second file
mv [file_name1] [file_name2] -> Rename [file_name1] to [file_name2] with the command
ln -s /path/to/[file_name] [link_name] -> Create a symbolic link to a file
touch [file_name] -> Create a new file
more [file_name] -> Show the contents of a file
cat [file_name] -> or use the cat command
cat [file_name1] >> [file_name2] -> Append file contents to another file
head [file_name] -> Display the first 10 lines of a file with
tail [file_name] -> Show the last 10 lines of a file
gpg -c [file_name] -> Encrypt a file
gpg [file_name.gpg] -> Decrypt a file
wc -> Show the number of words, lines, and bytes in a file

Directory Navigation

cd .. -> Move up one level in the directory tree structure
cd -> Change directory to $HOME
cd /chosen/directory -> Change location to a specified directory

File Compression

tar cf [compressed_file.tar] [file_name] -> Archive an existing file
tar xf [compressed_file.tar] -> Extract an archived file
tar czf [compressed_file.tar.gz] -> Create a gzip compressed tar file by running
gzip [file_name] -> Compress a file with the .gz extension

File Transfer

scp [file_name.txt] [server/tmp] -> Copy a file to a server directory securely
rsync -a [/your/directory] [/backup/] -> Synchronize the contents of a directory with a backup directory using the rsync command

