## The task is install and start the nginx

# write a playbool start with --- hypen indicate it is yaml file

    ---  
    -name: install and start nginx
     hosts: all
     become: root
    
     tasks:
     - name: Install nginx
       apt:
         name: nginx
         state: present
     tasks:
     -name: Start nginx
      service:
            name: nginx
            state: started
       

