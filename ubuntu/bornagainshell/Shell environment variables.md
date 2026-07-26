## Shell Environment Variables

I previously thought that everything put into the command line was a command overall. $OLDPWD is an [shell environment variable] , while [mkdir] is a command.

# Core Distinction

A command is an instruction that tells the shell to perform a specific action or run a program [ ls, cd, grep ]. When you type a command the shell executes it immediately.

A shell environment variable is a [ named storage container that holds data ] such as texts, numbers, paths for later use. It does not perform an action itself; instead [ it stores values that commands or scripts can read ].

# EXAMPLE 1

[$OLDPWD] stores a directory path, BUT typing $OLDPWD alone does not change directories; you need to combine it with a command such as [ cd $OLDPWD ].

# environment variables

$HOME : Predefined by the system to store the path to the current user's home directory.

$PWD : Is a standard shell environment variable that stores the absolute pathname of the current working directory.

# Remember

- Commands are executable programs or built-in functions available in the environment. 

- Environment variables are not executable commands on their own.
