# environment variables (shell variables)

'''bash
env
'''

env "show me everything" command

env command looks through the memory of your current shelll session and lists every variable that has been exported [meaning it is shared with programs and processes that your shell might start.] shows you the background settings that your Linux environment is currently using.

# Why it's useful

[ These variables are like "configuration profiles" for your terminal. They tell programs where to look for files, what language to use, or where your home directory is located. By running env, you can see exactly how your environment is configured right now. ]

- Child access in Linux environment variables refers to the ability of a newly started program (a "child" process) to read configuration data set by the program that launched it (the "parent"). 

# what does child access have to do with environment variables?

- When you type a command in your terminal, your shell creates a temporary child process to run that command. Environment variables act like a shared backpack that the parent hands to the child.  This backpack contains key-value pairs (like PATH or HOME) that tell the new program where to look for files or who the current user is.

Inheritance: The child process gets a copy of the parent’s environment variables at the moment it starts. 

Isolation: Changes the child makes to these variables do not affect the parent shell.  For example, if a script changes an environment variable, that change disappears when the script finishes.Inheritance: The child process gets a copy of the parent’s environment variables at the moment it starts. 

Isolation: Changes the child makes to these variables do not affect the parent shell.  For example, if a script changes an environment variable, that change disappears when the script finishes.

Exporting: By default, variables are local to the current shell. You must use the export command to place a variable into the "backpack" so it is available to any child processes or scripts you run. 

Exporting: By default, variables are local to the current shell. You must use the export command to place a variable into the "backpack" so it is available to any child processes or scripts you run. 

# echo $PATH

[ PATH ] variable lists dirs where the sys looks for executable progs. Each dir is seprarted by a colon :

# export

[ export MY_ENV_VAR="This is an env variable" ] The export command makes the [ variable ] available to child processes. 

- a shell script is a an executable prog?

[ echo 0$ ]

in Linux/bash scripting [ $0 ] is a special positional parameter that holds the name of the currently executing script or shell.

'''bash
echo $0
'''

output : usr/bin/bash

Inside a script: It expands to the filename or path used to invoke the script (e.g., ./myscript.sh or /usr/local/bin/script). 

In the interactive shell: It displays the name of the current shell (e.g., /bin/bash or /bin/zsh). 

Usage: It is commonly used to display usage messages, handle errors, or determine the script's directory for relative path resolution.

after using nano ~/.zshrc use command [ source ] to read and execute in current shell environment - so that [ changes take effect immediately ] 

    this is different from running file using [ bash ~/.zshrc ]
    which would run script in a [ new shell, and not effect 
    the current one. 
    
- also use [ ps -p $$ ] this displays the process status fo the current shell's proccess id [ PID ] explicitly identifying the active shell.

[echo $SHELL] only shows user's default login shell, which may differ
                from the shell currently active in your term.
    
# unset


[ unset -v $MY_ENV_VAR  ]

- unset is used to remove a variable from current session.

- -v flag tells system to see [ MY_ENV_VAR ] as a variable not
    a shell function
    
- [ MY_ENV_VAR ] is an environment variable
