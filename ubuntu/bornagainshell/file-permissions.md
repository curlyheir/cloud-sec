## File Permissions

# touch

'''bash
touch
'''
Creates a file & updates existing ones.

# cp

'''bash
cp 1st.text 1st_copy.txt
'''

[cp] copies the first argument [source file], the second is the destination.


'''bash
cp - r <directory> Desktop/
'''

- with this command we copied a directory and its content.

# chown

'''bash
chown
'''

Change file & directory ownership.

# chmod

'''bash
 sudo chmod 750 /home/greensignal/Desktop/beagainshell.txt
'''

Modify file & directory permissions numerically, & symbolically. [750] is shorthand way to set permissions.

7 (owner) : read (4) + write (2) + execute (1) = 7

5 (group) : read (4) + execute (1) = 5

0 (others) : no permissions

# Notes

- There is a difference between chown & chmod.
- look at the code before running it.

