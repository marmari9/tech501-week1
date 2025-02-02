# important linux commands:

- pwd: Print the current working directory. you should get the path.
- ls: List files and directories in the current directory.
- ls -a: Show all files, including hidden ones.
  - example: .ssh (start with . is hidden)
- ls -l: List files with detailed information (permissions).
- ls -al: Combine -a and -l to show all files with their permission.
- cd: Change directory.
- cd ..: Move to the parent directory.
- cd ~: Go to the home directory.
- cd /: Go to the root directory.
- cd ../..: Move up two directory levels.
- curl: Transfer data from/to a server (download files).
- wget: Download files from a URL.
- mv: rename files, or move files ( end the comand with / or it will rename instead). 
- cp: copy files  
- rm: remove files
- rm -r: remove directory (forced remove for dir/files with content)
- rm dir: works only on empty directory
- nano: text editor 
  - ctrl+ s: save 
  - Ctrl+ x:
  - exit
- cat: read content of files
- touch: create a file
- rmdir --help: help
- head : shows the first 10 lines of a file, for a specific line ; head -n
- tail: shows the last 10 lines of a file, for a specific line ; tail -n
- nl: displays a file's content with line numbers
- sudo su: login as a root user
- mv: move file to directory 
* revise absolute and relative paths
* to run a script follow these steps:
    - check permission : ls -l
    - change permission if needed: chmod +x(for execution) file.sh
    - advg is automation of commands like we did with Nginx 
- Environmental variables: accessed by Apps, can be cleared after app is done.
    - to create an envir variable: eg; export MYNAME=maram
    - printenv MYNAME(case-sensitive)
    - to add the variable to a .bashcr file (different for each user):
      - echo "export MYNAME=maram_h" >>.bashrc (adds envi var to the end of the file).
      - tail -3 .bashrc (last 3 lines of bashcr file)
      - source .bashcr: apply updates to .bashrc without restarting your terminal


# Generating a key pair for ssh:
- mkdir .ssh
- cd .ssh
- check dir path ; pwd 
- ssh-keygen -t rsa -b 4096 -c "maramalhmaidi@gmail.com"
- tech501-maram-az-key
- enter twice. 
- ls to check keys generated (public and private).


### Linux process:
## Process view commands:
- use ps : lists all processes.
- ps --help simple : lists the commands to use with processes.
- ps -e or ps -A : Lists all processes.
- **ps aux**: list all processes, most used command.
- top : rank processes by CPU usage.
    - use shift + M: to rank by memory usage.
    - use shift + N : to show newest process.
    - use shift +P : to go back showing most CPU usage.
- **top shows real time view of processes.**

## Process Kill Commands:
* If we created a sleep process like " sleep 5000 & "; & referes to the background(daemon?). follow the sequence:
  - **jobs** to show the number and PID of the process. 
  - **sudo systemctl status nginx**: show if the processes is running. 
  - **sudo systemctl stop nginx**: will stop the process.
  - **sudo systemctl start nginx**: will restart the process.
- There is 3 kill processes:
    1- Kill -l (PID): the softest kill. called **hangup**
    2- kill or kill -15 (PID): Gracefully medium kill **terminate**
    3- kill- 9 (PID): **killed** brutally kill
- Zombie process: where the parent pocess is killed and the child process is running in memory(app shows still running) so you have to terminate manually. 
- we use PM2 as a process manager ( if the the child process is killed and the parent is still there the PM2 will create a new child process with a new PID). 



