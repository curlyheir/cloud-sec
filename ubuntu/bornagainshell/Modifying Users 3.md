## Modifying Users 3

# usermod -d 

'''bash
sudo usermod -d /home/mtemerald greenshield 
'''

[ usermod ] is the command to modify the user, while the flag [ -d ] gives the command the option to change user's [ home/directory ] .

- ADDTION

Add the [ -m (or --move-home) ] flag to automatically move the contents of the old home directory to the new one and create the new directory if it doesn't exist.

# usermod -s

'''bash
sudo usermod -s /bin/bash greenshield 
'''

the command [ usermod -s ] changes user's [ default login shell ]. 
 [ usermod -s ] command in Linux is used to change a user's default login shell. 
 
# userdel -r

'''bash
sudo userdel -r greenshield
'''

The  [ userdel -r ]c ommand removes a user account and recursively deletes their home directory and mail spool. 

the [ -r ] flag ensures the home directory (/home/username) and the mail spool (typically in /var/spool/mail/) are permanently deleted.
