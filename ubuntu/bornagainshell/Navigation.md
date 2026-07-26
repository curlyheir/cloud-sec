## Navigation

# pwd

'''bash
pwd
'''

displays current location in file system.

# echo


'''bash
echo ~
'''

displays the path to your home directory.


# ls

'''bash
ls
'''

displays a list of the files & directories in your current working directory.


'''bash
ls ~
'''

lists the contents of your home directory, which may be different from your current working directory.

'''bash
ls *.txt
'''

lists all .txt files

'''bash
ls *.md
'''

lists all .md files

'''bash
ls note*
'''

lists all files [beginning with "note"] (the asterisk is after string)

'''bash
ls ..
'''

lists files in the [ .. ] parent directory [ one level up ].

# ls --help

'''bash
ls --help
'''

Usage: ls [OPTION]... [FILE]...
List information about the FILEs (the current directory by default).
Sort entries alphabetically if none of -cftuvSUX nor --sort is specified.

note: This tells you that ( ls is used to list information about files and directories.) The square brackets [] indicate optional parts. So [OPTION]... means you can use zero or more options, and [FILE]... means you can specify zero or more [files or directories.]

# Note 

[ Wildcards are powerful tools for working with groups of files.] The most common wildcards are:

*: Matches any number of characters
?: Matches any single character
[abc]: Matches any one character listed in the brackets


# cd

'''bash
cd ..
'''

This command moves you up one to your parent directory.

'''bash
cd ~
'''

This moves you to your home directory.

'''bash
cd project
'''

This moves you to your project directory.


'''bash
cd /home/project
'''

 this is an "absolute path" it starts from the root (/) & gives full location.
 
# Linux file system structure

cd means "change directory". The / takes you to the root directory.
[ cd / ]
[ cd ..] .. is the parent dir
[ cd ~ ] Go to home directory
[ cd - ] Go to previous directory
[ cd # ] go to home dir 


 /home is where user directories are stored. Each user typically has their own directory here.

/etc contains system configuration files.

/bin holds essential command binaries (programs) that need to be available for all users.

# tree

'''bash
sudo tree project
'''

- tree gives us a visual of a directory structure

# Notes
- Understanding my environment, by navigation is crucial.
- even the space that I cannot see has a value.
