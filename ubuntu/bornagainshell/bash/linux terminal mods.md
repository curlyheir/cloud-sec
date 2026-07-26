## linux terminal mods

# change ($) symbol

you can swap the dollar sign ($) in the Ubuntu terminal. 
That symbol is part of your shell prompt [ specifically the PS1 variable in Bash ], which indicates you are logged in as a standard user.  A hash (#) typically indicates a root user.

you must edit your shell configuration file [ ~/.bashrc ]

'''bash
nano ~/.bashrc
'''

- Scroll to the bottom of the file and add a line defining your new PS1. For example, to change it to #

'''bash
export PS1="# " 
'''

- Blue text for the path, reset color, then the symbol

export PS1="\[\e[34m\]\w\[\e[0m\] $ "

- Save the file (in Nano: press Ctrl+O, then Enter) and exit (Ctrl+X).

- apply changes

source ~/.bashrc

# if you can't see your username@hostname

nano ~/.bashrc

# Displays: username@hostname:current_directory ➜ 

export PS1="\u@\h:\w ➜ "

- Replace ➜ with whatever symbol you prefer. 

# With Colors (Optional): If you want the name in color (e.g., green) and the directory in blue:

export PS1="\[\e[32m\]\u@\h\[\e[0m\]:\[\e[34m\]\w\[\e[0m\] ➜ "

Save (Ctrl+O, Enter) and exit (Ctrl+X), then run:

source ~/.bashrc 

# what is xterm?

xterm is the standard, lightweight terminal emulator for the X Window System (X11) on Linux and Unix-like operating systems. Originally developed in 1984 by Mark Vandevoorde and currently maintained by Thomas Dickey, it provides a graphical window that emulates traditional hardware terminals such as the DEC VT102, VT220, and Tektronix 4014. 

Key characteristics include:

Functionality: It runs a command-line shell (like Bash) within the X graphical environment, allowing users to execute commands and manage the system. 

Architecture: Each xterm window operates as a separate process, enabling multiple independent terminal sessions within a single display. 

Customization: It supports extensive configuration via command-line arguments, X resources files (e.g., ~/.Xresources), and control menus accessed via Ctrl+mouse clicks. 

Usage: While modern desktop environments often default to other emulators (like GNOME Terminal or Konsole), xterm remains a ubiquitous fallback due to its minimal resource usage and stability, making it ideal for remote X sessions or low-resource systems. 

<https://invisible-island.net/xterm/>

<https://www.youtube.com/watch?v=07Q9oqNLXB4>
