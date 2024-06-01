# Further on User management
##  advanced user commands
* to know the machine - hostname
* to know the user name - whoami
* to add the user - sudo adduser username || sudo useradd username :- to add user into home directory creating by useradd -  sudo mkhomedir_helper username
- to change user password - sudo passwd username
- to change user id - sudo usermod -u newid(79403) username
- more info for users - cat /etc/passwd
- to delete the user - sudo userdel -r username
- to change and logged in other users in terminal - su - username  && to out - exit

## Sudoers file
- sudoers file is a file that give permission to other different users.
- to give access - sudo visudo
- then go to # user privilege specification 
- after that username ALL=ALL
- to change a shell - sudo usermod username -s /bin/bash
- to rename files and folders - mv oldfilename newfilename
## Linux file permission

- to list a files permission - ls l
- there are two permission
    -Owner
    -Permission 
- ownership is the owner of a file
- there are two kinds
    -user
    -group
- to change owner
    -sudo chown changedusername filename
- to change owner and group
    -sudo chown changedusername:changedgroup  filename
## Permission
- three types of permission
  -read(r)
  -write(w)
  -execute(x)
- if the permission began in "d" that is a folder else "-" it is a file
- permission have three parts
    -user-group-other
    -user(u) - rwx
    -group(g) - r-x
    -other(o) - r-x
    -All(a)
-  command to change permission of  file                                                                                                                                                                                                       **+** is giving permission
   - we use chmode to change permission                                            - is removing permission
    -sudo chmod + or -<option>(x ,w ,r) filename .
    - read - 4 - r
    - write -2 -w
    - execute - 1 -x
    - chmod <parameter> filename
- the parameter can be in number and symbol

1.  Parameters in symbol

- chmod a+x filename   ->  adding execute permission for all  ( chmod +x filename)

- chmod u+x filename -> adding execute permission for user
    
- chmod g+x filename -> adding execute permission for group
    
- chmod o+x filename -> adding execute permission for other
    
- chmod -x filename -> removing execute permission for all

- chmod a+rwx , u-rw , g-x , o-xw filename -> gives rwx for all and removes something from all
   
2. Parameters in Number

- chmod 621 filename -> 6 for user, 2 for group, 1 for other  ( 6 = 4+2 ),  6 =r w
    
- chmod 777 filename -> 7 for users, 7 for group , 7 for others (7 =4+2+1),  7 = rwx
    

