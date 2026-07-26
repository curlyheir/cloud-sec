## green log

Welcome to my green log. This is where I share my experience, beyond the shell & random things relative to linux.

# 1
I was trying to screenshot my shellwork coming from using a windows os. Obviously not the same os keyboard shortcut. Learning by doing, & reapplying what I knew to what I need to do now. settings-keyboard-keyboard shortcut, rerouted Fkey 1,2,3 keys to screenshot. Problem solved.

- [gnome-screenshot] in modern Ubuntu versions (22.04 and later), the standalone gnome-screenshot application was removed and replaced by a built-in GNOME Shell extension. 

Storage: Images are saved to ~/Pictures/Screenshots/ by default.

# 2

With each .md, and or notes screenshot my shell to show work. SEEing and DOing is doing & seeing. Helps me grasp and implement concepts.

text editors are lightweight and swift. help keep the modification speed, thought process speed balanced.

destination is important even with explaining how something works. There is always a destination.

spellcheck can cripple workforce

eversince I switched from windows to ubuntu, I am learning alot more.

# 3

Directories are just doors; it is what my purpose is with the access that gives commands context.

Ubuntu won't let me move a screenshot from ~ to a desktop folder

- Explanation

The issue likely stems from GNOME Shell’s hardcoded screenshot behavior in recent Ubuntu versions (20.04+), where the default screenshot tool ignores gsettings configurations and forces saves to the $HOME/Pictures directory.  Because the file is created by the system daemon, you may encounter permission issues or the file may not appear immediately in the source folder if the save path is misconfigured

In modern Ubuntu (22.04 and later), the system uses a specific sub-directory logic that ignores the general Pictures setting for screenshots. 

- Working Work Around

1. Remove the default subfolder

'''bash
rm -rf ~/Pictures/Screenshots
'''

2. Create a symbolic link named Screenshots that points directly to the Pictures folder

'''bash
ln -s ~/Pictures ~/Pictures/Screenshots
'''
- Result : When the system tries to save to [ ~/Pictures/Screenshots ] , it will actually drop file to [ Desktop ]. 

In modern Ubuntu (22.04 and later), the system uses a specific sub-directory logic that ignores the general Pictures setting for screenshots. 

at this point I am now trying to move a .png file using [ mv ] to a git folder on my desktop monitored by [GITKRAKEN]. Due

'''bash
sudo apt-get update
'''

'''bash
sudo apt-get install git-lfs
'''

'''bash
git lfs intall
'''

'''bash
chmod +w ~/Pictures/Screenshots/fix.png
'''

'''bash
mv ~/Pictures/Screenshots/fix.png ~/Desktop/cloud-security/linux
'''

# Simple Breakdown

1. The Hidden Rule: The repo’s .gitattributes file told Git: "Treat PNGs as special binary files. If they aren't explicitly 'locked' by a user, make them Read-Only to prevent accidents."

2. The Problem: Without git-lfs installed, your terminal didn't know how to handle this rule. GitKraken likely flagged the file as "in use" or "protected," and the OS enforced the Read-Only status, blocking the mv command.

3. The Fix: Installing git-lfs and running git lfs install taught your system how to read those rules. It likely automatically corrected the file permissions (making it writable) or allowed GitKraken to properly release its lock, enabling the move.

In short: The .txt file had standard permissions, but the .png was waiting for the LFS tool to unlock it.


ngl this was difficult for me it took me a few hours to wrap my head around the issue because it was layered. Not only did i have to move the screenshot save to the desktop (while tricking it) but chmod file permissions for moving .png files through git folders. with some research and trial/error I got it done. check ubuntuscreenshotsavelocationfix.png & gitkrakenpnglockfix.png for the shellshot.

shellshot - a screenshot of shellcode.

# 4

Using brace expansion for the first time to move multiple pngs
mv -v -- *.png /path/to/new/folder/

while pasting some oldcode into shell, while pressing up and down arrows (after pressing the right arrow to solidify paste, but before using left arrow to push cursor back to where I want to change file name) it switched between an array of old lines I just typed into the command line how?

Spaces between commands matter! I was getting ssh configured, and the space between the url and command made output display usage instead of execution.

- Configured secure GitHub SSH authentication on Ubuntu, migrated a repository from HTTPS to SSH, & resolved Git authentication & branch synchronization issues using the Linux command line.

- tried [ git mv ] to move files in working directories monitored by gitkraken.

- [ grep -r "string" ] I need to remember this.

- [ cat ] is short for concatenate (display file contents).

- Concatenate means to connect or link in a series or chain. But in computers to arrange [input] (strings of characters) into a [output] chained list.

- commands [cp,mv,rm] are some of the most frequently used day-to-day linux ops.

- up arrow key (↑) to recall the last command you typed.

- use tab completion in bash to save time, and avoid spelling errors

- read man and practice using flags

- when organizing information it sticks. my belief that all forms of content have a place. When data is put in its place, that container is a reinforcement for memory to texturalize that piece of info.

- What exactly is a string again?

- In the context of Bash and POSIX-compliant shells, a string is specifically defined as a contiguous sequence of bytes terminated by and including the first null byte.

- Linux is a multi-user operating system. This means multiple users can use the same Linux computer simultaneously, each with their own private space and files, while also sharing some system resources. 

- sucessfully used [cp] to [change file type from .txt to .md] and wrote in it using [echo "" >> filename] [echo " text here " > filename]

- understanding what the terminal is, is key to truly grasping commands, pipes, flags etc. The value of characters, and what they mean, what they can do ; their weight, measurement in time = value changes.

- The terminal character device files connect the kernel to the input and output.
The critical interface connecting the kernel to input and output hardware.

When a user interacts with hardware (like pressing a key on a keyboard), the CPU triggers an interrupt, causing the kernel's device driver to execute.

interrupt is a signal sent to the CPU by hardware or software indicating that an even requires immediate attention. 

The driver translates this hardware signal into data stored in the character device file (e.g., /dev/input/event0). 

User-space programs then read from this file to receive the input.  Conversely, when a program needs to output data (like displaying text), it writes to the device file, and the kernel driver translates those bytes into signals the hardware understands. 

- fixed fake usb in terminal

- sudo apt install nala to speed up package fetching and downloading

- learned [ ctrl + R fuzzy historal search ]

[ enter ] to accept the selected command for editing.

- run bleachbit every six months

- make a log script instead of this, which a widget that floats on desktop if possible.

- disabled [ export BASH_IT_THEME="" ] in nano ~/.bashrc
