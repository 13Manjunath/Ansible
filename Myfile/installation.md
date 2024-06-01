## INSTALLATION OF ANSIBLE AND SET UP

 configure the 2 aws instances. one is ansible server and onather one is target server 
 connect to your local terminal

 # installation
 ---> for the ansible server create on folder and then apply cmd
  
    sudo apt update
    sudo apt install ansible
 # for the passwordless athentication 
 ---> in the ansible server  do---
 
     ssh-keygen 
     
     ls location of file
--it will generate a public key and private key Then 

      cat ---location of the file--- -public-key

 --it gererates the public key and copy that--

 ## login in onather terminal of target server 

      ssh-keygen
 --it will also create a keys --and check--
 
      ls ~/.ssh/

  --it will shows the authored keys then 
     
      vim ~/.ssh/authorised_keys

# paste the content copy form the ansible server here --and save it

 -- then in the ansible server apply the command--

      ssh _target server ip adress
   # --successifully logined to the target server--
  
