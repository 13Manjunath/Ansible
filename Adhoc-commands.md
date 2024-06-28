## To create a file in the target server 
        ansible -i inventory all -m "shell" -a "touch target-server"

## Ping all hosts:
This command uses the ping module to check the connectivity of all hosts defined in the inventory.
        ansible all -m ping

## Gather facts from all hosts:
This command collects and returns all the facts from the managed nodes.
        ansible all -m setup
    
## Execute a command on all hosts:
The command module is used here to run the uptime command on all hosts.
        ansible all -m command -a "uptime"

## Copy a file to all hosts:
The copy module is used to copy a file from the local machine to all the managed nodes.
        ansible all -m copy -a "src=/path/to/local/file dest=/path/to/remote/file"

## Create a user on all hosts:
The user module is used to create a new user with the specified name and password.
        ansible all -m user -a "name=username password=secret"

## Check disk space on all hosts:
The shell module is used to execute the df -h command, which displays the disk space usage.
        ansible all -m shell -a "df -h"

## Check System Uptime:
Quickly check the uptime of all managed nodes to monitor system stability.
        ansible all -m command -a "uptime"

## Reboot Servers:
Reboot all servers, often necessary after updates or configuration changes.
        ansible all -m reboot -b

## Add a New User:
Add a new user across all managed nodes.    
        ansible all -m user -a "name=newuser state=present" -b

