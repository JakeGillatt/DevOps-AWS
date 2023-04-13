# List of Linux commands

- `ls` displays the folders and files in the current directory
- `ls - a` displays all files and folders including hidden items in the current directory
- `whoami` displays the operating system info
- `pwd` shows the current directory (dir) location
- `uname -a` shows all the info associated with the username
- `mkdir` creates a new folder in the current dir
- `cd 'folder name'` change dir location to the specified folder
- `cd ..` moves the current dir location one step back
- `touch 'file name'` creates a new file in the current dir
- `nano 'file name'` edit the file (use CTRL + X to save the file)
- `cat 'file name'` displays the contents of the file
- `cp 'file name' 'dir'` copies the file to the specified dir
- `rm 'file name'` deletes the specified file
- `mv 'file name' 'dir'` moves the file to the specified dir
- `ll` displays the files permissions
- `chmod 'code' 'file name'` changes the files permissions (use a chmod calculator to get the code)
- `sudo` gives admin permission to a command
- `top` lists all the current processes like a task manager
- `history` displays the previously entered commands
- `head -1 'file name'` prints the first line from the file
- `nl 'file name'` asigns numbers to each line of text
- `tail -1 'file name'` prints the last line from the file
- `sort 'filename'` sort the content in alphabetical order
- `cat 'filename' | grep 'content'` searches file for specific content and prints it out
- `sudo su` enters into Admin mode
- `apt` package manager
- `sudo systemctl stop/start nginx` used to stop/start process
- `sudo apt install nginx` install nginx
- `sudo apt update/upgrade -y` used to update/upgrade services. -y will automate responce "Yes"
- `service nginx status` check the status of nginx service

script to automate update/upgrade, installation and enabling of nginx:
sudo touch provision.sh - create a scipt file

`sudo nano provision.sh` - open the file with nano

use follwing to add to your script:

#!/bin/bash

`sudo apt update -y`

`sudo apt upgrade -y`

`sudo apt install nginx -y`

`sudo systemctl restart nginx`

`sudo systemctl enable nginx`

`sudo chmod +x provision.sh` - make file executable

`sudo ./provision.sh` - execute file
