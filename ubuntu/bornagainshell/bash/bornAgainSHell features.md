## bornAgainSHell features

[ type (command input) and press tab ]

# Tab completion in Linux is a shell feature that auto-fills commands, file paths, or arguments when you press the Tab key, significantly reducing typing errors and effort. 
 
 In Bash, it is powered by the Readline library and the complete builtin, which can use standard filename matching or programmable completion functions (often provided by the bash-completion package) to handle context-specific suggestions like git branches or command options.

# stop an active running process

[ctrl + c] stops a running process and returns you to your terminal prompt.

[ctrl + l] clears the terminal screen.

# type

'''bash
type ls
'''
output: [ls --color=tty)

It means that when you input [ls] you're actually running [ ls --color=tty ].
An alias is like a shortcut or nickname for a command. In this case, the 
[ ls command is set up to always use colors in its output. ]

'''bash
type cd
'''
output: [cd is a shell builtin] 

The [type] command in Linux is used to display how the shell interprets the command you provide. Think of it as an "identity check" for the commands you type into your terminal. ["command id, command identity".]

# type system logic 

The logic here is to help you distinguish between [commands that live inside the shell environment] and [commands that are configured as shortcuts or external programs.] This is a very useful way to learn more about how your terminal is set up.

# man navigation

'''bash
man grep
'''

note : you're now in the manual viewer

- use up and down arrow keys to scroll line by line
- space bar & fkey to move forward one page
- bkey to move back one page
- /followed by a word to search for that word in the manual for example. [ /file ]
will search for "file".
- nkey move to the next occurrence of your search term.
- Nkey to move to previous occurrence of your search term.


