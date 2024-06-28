## to create a file in the target server 
    ansible -i inventory all -m "shell" -a "touch target-server"
