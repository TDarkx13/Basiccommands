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

Git.
Git is the free and open source distributed version control system that's responsible for everything GitHub related that happens locally on your computer. This cheat sheet features the most important and commonly used Git commands for easy reference.

SETUP
Configuring user information used across all local repositories.

git config --global user.name “[firstname lastname]” -> set a name that is identifiable for credit when review version history
git config --global user.email “[valid-email]” -> set an email address that will be associated with each history marker
git config --global color.ui auto -> set automatic command line coloring for Git for easy reviewing

SETUP & INIT
Configuring user information, initializing and cloning repositories.

git init -> initialize an existing directory as a Git repository
git clone [url] -> retrieve an entire repository from a hosted location via URL

INSPECT & COMPARE
Examining logs, diffs and object information.

git log -> show the commit history for the currently active branch
git log branchB..branchA -> show the commits on branchA that are not on branchB
git log --follow [file] -> show the commits that changed file, even across renames
git diff branchB...branchA -> show the diff of what is in branchA that is not in branchB
git show [SHA] -> show any object in Git in human-readable format

TRACKING PATH CHANGES
Versioning file removes and path changes.

git rm [file] -> delete the file from project and stage the removal for commit
git mv [existing-path] [new-path] -> change an existing file path and stage the move
git log --stat -M -> show all commit logs with indication of any paths that moved

STAGE & SNAPSHOT
Working with snapshots and the Git staging area.

git status -> show modified files in working directory, staged for your next commit
git add [file] -> add a file as it looks now to your next commit (stage)
git reset [file] -> unstage a file while retaining the changes in working directory
git diff -> diff of what is changed but not staged
git diff --staged -> diff of what is staged but not yet commited
git commit -m “[descriptive message]” -> commit your staged content as a new commit snapshot

BRANCH & MERGE
Isolating work in branches, changing context, and integrating changes.

git branch -> list your branches. a * will appear next to the currently active branch
git branch [branch-name] -> create a new branch at the current commit
git checkout -> switch to another branch and check it out into your working directory
git merge [branch] -> merge the specified branch’s history into the current one
git log -> show all commits in the current branch’s history

SHARE & UPDATE
Retrieving updates from another repository and updating local repos.

git remote add [alias] [url] -> add a git URL as an alias
git fetch [alias] -> fetch down all the branches from that Git remote
git merge [alias]/[branch] -> merge a remote branch into your current branch to bring it up to date
git push [alias] [branch] -> Transmit local branch commits to the remote repository branch
git pull -> fetch and merge any commits from the tracking remote branch

REWRITE HISTORY
Rewriting branches, updating commits and clearing history.

git rebase [branch] -> apply any commits of current branch ahead of specified one
git reset --hard [commit] -> clear staging area, rewrite working tree from specified commit