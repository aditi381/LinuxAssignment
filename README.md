Q1.	Create a directory named "MyFiles" in your home directory. Navigate into this directory and list its contents.
aditi@aditi-VirtualBox:~$ mkdir ~/MyFiles
aditi@aditi-VirtualBox:~$ ls
a    b        document   Downloads   Music    MYFiles   Public  Templates
add  Desktop  Documents  fileeaditi  MyFiles  Pictures  snap    Videos

Q2.	Copy a file named "document.txt" from your home directory to the "MyFiles" directory. Move the file to a subdirectory named "Documents" within "MyFiles."
aditi@aditi-VirtualBox:~$ cp ~/Documents/document.txt ~/MyFiles
aditi@aditi-VirtualBox:~$ mv ~/MyFiles/document.txt ~/MyFiles/Documents
aditi@aditi-VirtualBox:~$ ls
a    b        Documents  fileeaditi  MyFiles   Public  Templates
add  Desktop  Downloads  Music       Pictures  snap    Videos

Q3.	Create an empty file named "notes.txt" in the "MyFiles" directory. Afterward, delete the file.
aditi@aditi-VirtualBox:/home$ ln ~/MyFiles/Documents/document.txt ~/MyFiles/Documents/hardlink.txt
ln: /home/aditi/MyFiles/Documents/document.txt: hard link not allowed for directory
aditi@aditi-VirtualBox:/home$ ls
aditi

Q4.	Create a hard link named "hardlink.txt" for the file "document.txt" within the "Documents" subdirectory. Also, create a symbolic link named "symlink.txt" in the same location.
aditi@aditi-VirtualBox:/home$ ln ~/MyFiles/Documents/document.txt ~/MyFiles/Documents/hardlink.txt
ln: /home/aditi/MyFiles/Documents/document.txt: hard link not allowed for directory
aditi@aditi-VirtualBox:/home$ ln -s ~/MyFiles/Documents/document.txt ~/MyFiles/Documents/symlink.txt

Q5.	In the "MyFiles" directory, use a single command to list all files that start with the letter "a" and have a ".txt" extension.
aditi@aditi-VirtualBox:/home$ ls ~/MyFiles/a*.txt
aditi@aditi-VirtualBox:/home$ ls
aditi

Q6.	Rename all files in the "Documents" subdirectory of "MyFiles" with a ".bak" extension. Ensure the original file names are preserved.
aditi@aditi-VirtualBox:/home$ cd ~/MyFiles/Documents  # Navigate to the "Documents" subdirectory
for file in *; do mv "$file" "$file.bak"; done
aditi@aditi-VirtualBox:~/MyFiles/Documents$ ls
document.txt.bak  symlink.txt.bak

Q7.	Use a wildcard character to copy all files from the "Documents" subdirectory of "MyFiles" to another directory named "Backup."
aditi@aditi-VirtualBox:~/MyFiles/Documents$ cp ~/MyFiles/Documents/* ~/Backup/
cp: target '/home/aditi/Backup/' is not a directory

Q8.	Execute the ls command to list files in the current directory. Save the output to a file named "file_list.txt." Then, use a pipe to filter the output through grep to display only files with a ".txt" extension.
aditi@aditi-VirtualBox:~/MyFiles/Documents$ ls > file_list.txt
aditi@aditi-VirtualBox:~/MyFiles/Documents$ cat file_list.txt | grep '\.txt$'
file_list.txt
aditi@aditi-VirtualBox:~/MyFiles/Documents$ cat file_list.txt | grep '\.txt$'
file_list.txt
aditi@aditi-VirtualBox:~/MyFiles/Documents$ ls | tee file_list.txt | grep '\.txt$'
file_list.txt

Q9.Create a new text file named "my_notes.txt" using the touch command. Open the file in the Vim editor, add some text, and save the changes.
aditi@aditi-VirtualBox:~/MyFiles/Documents$ touch my_notes.txt
aditi@aditi-VirtualBox:~/MyFiles/Documents$ vim my_notes.txt
Command 'vim' not found, but can be installed with:
sudo apt install vim         # version 2:8.2.3995-1ubuntu2.13, or
sudo apt install vim-tiny    # version 2:8.2.3995-1ubuntu2.13
sudo apt install neovim      # version 0.6.1-3
sudo apt install vim-athena  # version 2:8.2.3995-1ubuntu2.13
sudo apt install vim-gtk3    # version 2:8.2.3995-1ubuntu2.13
sudo apt install vim-nox     # version 2:8.2.3995-1ubuntu2.13
aditi@aditi-VirtualBox:~/MyFiles/Documents$ These are my notes.
This is some example text.
These: command not found
This: command not found
aditi@aditi-VirtualBox:~/MyFiles/Documents$ i
i: command not found
aditi@aditi-VirtualBox:~/MyFiles/Documents$ "i"
i: command not found
aditi@aditi-VirtualBox:~/MyFiles/Documents$ sudo apt install vim         # version 2:8.2.3995-1ubuntu2.13
[sudo] password for aditi: 
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
  vim-runtime
Suggested packages:
  ctags vim-doc vim-scripts
The following NEW packages will be installed:
  vim vim-runtime
0 upgraded, 2 newly installed, 0 to remove and 51 not upgraded.
Need to get 8,570 kB of archives.
After this operation, 37.6 MB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://in.archive.ubuntu.com/ubuntu jammy-updates/main amd64 vim-runtime all 2:8.2.3995-1ubuntu2.15 [6,835 kB]
Get:2 http://in.archive.ubuntu.com/ubuntu jammy-updates/main amd64 vim amd64 2:8.2.3995-1ubuntu2.15 [1,735 kB]
Fetched 8,570 kB in 57s (149 kB/s)                                             
Selecting previously unselected package vim-runtime.
(Reading database ... 199410 files and directories currently installed.)
Preparing to unpack .../vim-runtime_2%3a8.2.3995-1ubuntu2.15_all.deb ...
Adding 'diversion of /usr/share/vim/vim82/doc/help.txt to /usr/share/vim/vim82/d
oc/help.txt.vim-tiny by vim-runtime'
Adding 'diversion of /usr/share/vim/vim82/doc/tags to /usr/share/vim/vim82/doc/t
ags.vim-tiny by vim-runtime'
Unpacking vim-runtime (2:8.2.3995-1ubuntu2.15) ...
Selecting previously unselected package vim.
Preparing to unpack .../vim_2%3a8.2.3995-1ubuntu2.15_amd64.deb ...
Unpacking vim (2:8.2.3995-1ubuntu2.15) ...
Setting up vim-runtime (2:8.2.3995-1ubuntu2.15) ...
Setting up vim (2:8.2.3995-1ubuntu2.15) ...
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/vim (vim) in a
uto mode
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/vimdiff (vimdi
ff) in auto mode
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/rvim (rvim) in
 auto mode
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/rview (rview) 
in auto mode
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/vi (vi) in aut
o mode
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/view (view) in
 auto mode
update-alternatives: using /usr/bin/vim.basic to provide /usr/bin/ex (ex) in aut
o mode
Processing triggers for man-db (2.10.2-1) ...
aditi@aditi-VirtualBox:~/MyFiles/Documents$ i
i: command not found
aditi@aditi-VirtualBox:~/MyFiles/Documents$ sudo apt install vim         # version 2:8.2.3995-1ubuntu2.13
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
vim is already the newest version (2:8.2.3995-1ubuntu2.15).
0 upgraded, 0 newly installed, 0 to remove and 51 not upgraded.
Q10.	Run the date commanaditi@aditi-VirtualBox:~/MyFiles/Documents$ touch my_notes.txt
aditi@aditi-VirtualBox:~/MyFiles/Documents$ vim my_notes.txt
aditi@aditi-VirtualBox:~/MyFiles/Documents$ current_date=$(date)
aditi@aditi-VirtualBox:~/MyFiles/Documents$ echo "$current_date"
Sunday 04 February 2024 10:38:36 PM IST
aditi@aditi-VirtualBox:~/MyFiles/Documents$ echo "$current_date" >> my_notes.txt 
aditi@aditi-VirtualBox:~/MyFiles/Documents$ current_date=$(date)
echo "$current_date"
echo "$current_date" >> my_notes.txt
Sunday 04 February 2024 10:39:26 PM IST

Q11.	Edit the Bash startup script (e.g., .bashrc) to set an environment variable named "CUSTOM_PATH" to a specific directory path. Ensure the variable is available in new shell sessions.
aditi@aditi-VirtualBox:~/MyFiles/Documents$ nano ~/.bashrc
aditi@aditi-VirtualBox:~/MyFiles/Documents$ source ~/.bashrc
aditi@aditi-VirtualBox:~/MyFiles/Documents$ ls
document.txt.bak  file_list.txt  my_notes.txt  symlink.txt.bak
aditi@aditi-VirtualBox:~/MyFiles/Documents$

Q12.Use the echo command to add a new line of text to the "my_notes.txt" file without overwriting existing content. Verify that the new text is appended.
aditi@aditi-VirtualBox:~/MyFiles/Documents$ echo "This is a new line of text." >> my_notes.txt
aditi@aditi-VirtualBox:~/MyFiles/Documents$ cat my_notes.txt
Sunday 04 February 2024 10:38:36 PM IST
Sunday 04 February 2024 10:39:26 PM IST
This is a new line of text.
aditi@aditi-VirtualBox:~/MyFiles/Documents$ echo "This is a new line of text." >> my_notes.txt
cat my_notes.txt
Sunday 04 February 2024 10:38:36 PM IST
Sunday 04 February 2024 10:39:26 PM IST
This is a new line of text.
This is a new line of text.

Q13.	List all files in the "/etc" directory, filter the output to include only those containing the word "conf," and save the result to a file named "conf_files.txt."
aditi@aditi-VirtualBox:~/MyFiles/Documents$ ls /etc | grep 'conf' > conf_files.txt
aditi@aditi-VirtualBox:~/MyFiles/Documents$ ls /etc | grep -i 'conf' > conf_files.txt
aditi@aditi-VirtualBox:~/MyFiles/Documents$ ls
conf_files.txt  document.txt.bak  file_list.txt  my_notes.txt  symlink.txt.bak

Q14.	Open the "my_notes.txt" file in Vim. Use Vim's search and replace functionality to replace all occurrences of the word "important" with "critical." Save the changes.
E325: ATTENTION
Found a swap file by the name ".my_notes.txt.swp"
          owned by: aditi   dated: Sun Feb 04 22:34:05 2024
         file name: ~aditi/MyFiles/Documents/my_notes.txt
          modified: YES
         user name: aditi   host name: aditi-VirtualBox
        process ID: 15299 (STILL RUNNING)
While opening file "my_notes.txt"
             dated: Sun Feb 04 22:44:27 2024
      NEWER than swap file!

(1) Another program may be editing the same file.  If this is the case,
    be careful not to end up with two different instances of the same
    file when making changes.  Quit, or continue with caution.
(2) An edit session for this file crashed.
    If this is the case, use ":recover" or "vim -r my_notes.txt"
    to recover the changes (see ":help recovery").
    If you did this already, delete the swap file ".my_notes.txt.swp"
    to avoid this message.
-- More --
E325: ATTENTION
Found a swap file by the name ".my_notes.txt.swp"
          owned by: aditi   dated: Sun Feb 04 22:34:05 2024
         file name: ~aditi/MyFiles/Documents/my_notes.txt
          modified: YES
         user name: aditi   host name: aditi-VirtualBox
        process ID: 15299 (STILL RUNNING)
While opening file "my_notes.txt"
             dated: Sun Feb 04 22:44:27 2024
      NEWER than swap file!

(1) Another program may be editing the same file.  If this is the case,
    be careful not to end up with two different instances of the same
    file when making changes.  Quit, or continue with caution.
(2) An edit session for this file crashed.
    If this is the case, use ":recover" or "vim -r my_notes.txt"
    to recover the changes (see ":help recovery").
    If you did this already, delete the swap file ".my_notes.txt.swp"
    to avoid this message.
-- More --
E325: ATTENTION
Found a swap file by the name ".my_notes.txt.swp"
          owned by: aditi   dated: Sun Feb 04 22:34:05 2024
         file name: ~aditi/MyFiles/Documents/my_notes.txt
          modified: YES
         user name: aditi   host name: aditi-VirtualBox
        process ID: 15299 (STILL RUNNING)
While opening file "my_notes.txt"
             dated: Sun Feb 04 22:44:27 2024
      NEWER than swap file!

(1) Another program may be editing the same file.  If this is the case,
    be careful not to end up with two different instances of the same
    file when making changes.  Quit, or continue with caution.
(2) An edit session for this file crashed.
    If this is the case, use ":recover" or "vim -r my_notes.txt"
    to recover the changes (see ":help recovery").
    If you did this already, delete the swap file ".my_notes.txt.swp"
    to avoid this message.
-- More --
E325: ATTENTION
Found a swap file by the name ".my_notes.txt.swp"
          owned by: aditi   dated: Sun Feb 04 22:34:05 2024
         file name: ~aditi/MyFiles/Documents/my_notes.txt
          modified: YES
         user name: aditi   host name: aditi-VirtualBox
        process ID: 15299 (STILL RUNNING)
While opening file "my_notes.txt"
             dated: Sun Feb 04 22:44:27 2024
      NEWER than swap file!

(1) Another program may be editing the same file.  If this is the case,
    be careful not to end up with two different instances of the same
    file when making changes.  Quit, or continue with caution.
(2) An edit session for this file crashed.
    If this is the case, use ":recover" or "vim -r my_notes.txt"
    to recover the changes (see ":help recovery").
    If you did this already, delete the swap file ".my_notes.txt.swp"
    to avoid this message.
-- More --

Q15.	Create a new user account named "john_doe." Set the user's home directory to "/home/john_doe" and assign the user to the "users" group.
aditi@aditi-VirtualBox:~/MyFiles/Documents$ sudo ls /root
[sudo] password for aditi: 
snap
aditi@aditi-VirtualBox:~/MyFiles/Documents$ LS
LS: command not found
aditi@aditi-VirtualBox:~/MyFiles/Documents$ ls
conf_files.txt  document.txt.bak  file_list.txt  my_notes.txt  symlink.txt.bak
aditi@aditi-VirtualBox:~/MyFiles/Documents$

Q17.	Modify the user account "john_doe" to change the default shell to "/bin/bash" and set the account's expiration date to one month from today.
aditi@aditi-VirtualBox:~/MyFiles/Documents$ sudo usermod --shell /bin/bash --expiredate $(date -d "+1 month" +%Y-%m-%d) john_doe
aditi@aditi-VirtualBox:~/MyFiles/Documents$ grep john_doe /etc/passwd
john_doe:x:1001:100:Aditi Singh,111,1111,1111,33333:/home/john_doe:/bin/bash
aditi@aditi-VirtualBox:~/MyFiles/Documents$
Q18.	Create a new group named "development_team." Add "john_doe" to this group and verify the group's existence.
aditi@aditi-VirtualBox:~/MyFiles/Documents$ sudo groupadd development_team
aditi@aditi-VirtualBox:~/MyFiles/Documents$ sudo usermod -aG development_team john_doe
aditi@aditi-VirtualBox:~/MyFiles/Documents$ getent group development_team
development_team:x:1001:john_doe
aditi@aditi-VirtualBox:~/MyFiles/Documents$ grep development_team /etc/group
development_team:x:1001:john_doe
Q19.	Remove "john_doe" from the "users" group and add them to the "development_team" group. Confirm the changes.
aditi@aditi-VirtualBox:~/MyFiles/Documents$ sudo deluser john_doe users
/usr/sbin/deluser: You may not remove the user from their primary group.
aditi@aditi-VirtualBox:~/MyFiles/Documents$ sudo usermod -aG development_team john_doe
aditi@aditi-VirtualBox:~/MyFiles/Documents$ groups john_doe
john_doe : users development_team
Q20.	Delete the user account "john_doe" and ensure that their home directory is also removed.
aditi@aditi-VirtualBox:/home$ sudo passwd john_doe
New password: 
BAD PASSWORD: The password is a palindrome
Retype new password: 
passwd: password updated successfully
aditi@aditi-VirtualBox:/home$ getent passwd john_doe
ls /home/john_doe
john_doe:x:1001:1002::/home/john_doe:/bin/bash
aditi@aditi-VirtualBox:/home$

Q21.	Delete the group "development_team" and ensure that all users previously belonging to the group are appropriately handled.
aditi@aditi-VirtualBox:/home$ sudo groupdel development_team
aditi@aditi-VirtualBox:/home$ getent group development_team
aditi@aditi-VirtualBox:/home$ groups <username>
bash: syntax error near unexpected token `newline'
aditi@aditi-VirtualBox:/home$ groups john_doe
john_doe : john_doe

Q22.	Implementpassword policy that requires users to change their passwords every 90 days. Apply this policy to all existing and new user accounts.

aditi@aditi-VirtualBox:/home$ sudo chage -M 90 -I 90 -m 0 -W 14 -E -1 $(cut -d: -f1 /etc/passwd)
Usage: chage [options] LOGIN

Options:
  -d, --lastday LAST_DAY        set date of last password change to LAST_DAY
  -E, --expiredate EXPIRE_DATE  set account expiration date to EXPIRE_DATE
  -h, --help                    display this help message and exit
  -i, --iso8601                 use YYYY-MM-DD when printing dates
  -I, --inactive INACTIVE       set password inactive after expiration
                                to INACTIVE
  -l, --list                    show account aging information
  -m, --mindays MIN_DAYS        set minimum number of days before password
                                change to MIN_DAYS
  -M, --maxdays MAX_DAYS        set maximum number of days before password
                                change to MAX_DAYS
  -R, --root CHROOT_DIR         directory to chroot into
  -W, --warndays WARN_DAYS      set expiration warning days to WARN_DAYS
Q23.	Manually lock the user account "john_doe." Attempt to log in as "john_doe" to confirm that the account is locked. Then, unlock the account.
aditi@aditi-VirtualBox:/home$ sudo passwd john_doe
New password: 
BAD PASSWORD: The password is shorter than 8 characters
Retype new password: 
passwd: password updated successfully
Q24.	Use the id command to display detailed information about the "john_doe" user, including user ID, group ID, and supplementary groups.
aditi@aditi-VirtualBox:/home$ id john_doe
uid=1001(john_doe) gid=1002(john_doe) groups=1002(john_doe)

Q25.	Configure the password aging for the user "john_doe" to enforce a maximum password age of 60 days. Confirm that the changes take effect.
aditi@aditi-VirtualBox:/home$ sudo chage -M 60 john_doe
[sudo] password for aditi: 
aditi@aditi-VirtualBox:/home$ sudo chage -l john_doe
Last password change					: Feb 04, 2024
Password expires					: Apr 04, 2024
Password inactive					: never
Account expires						: never
Minimum number of days between password change		: 0
Maximum number of days between password change		: 60
Number of days of warning before password expires	: 7
