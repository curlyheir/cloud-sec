# env var 2

Yes, the export command is per session.

When you run export PATH="$PATH:$HOME/my_scripts", the change only applies to the specific terminal window or shell session where you typed it.

Why it works this way:
Temporary: The environment variable is stored in the memory of the current process. If you close your terminal or open a second terminal window, the new path will not be there.
Non-Permanent: This is a safety feature; if you make a mistake in your PATH, it won't permanently break your system settings. Once you log out or restart, your shell configuration resets to its default state.
How to make it permanent:
If you want this change to apply every time you open a new terminal, you need to add this exact line to your shell's configuration file (such as .zshrc or .bashrc). By placing it in those "start-up" files, the system will automatically run the export command every time a new session begins.



It works with the direct path (like ./hello.sh or /home/labex/my_scripts/hello.sh) because you are giving the computer the exact address of the file. In this case, the computer doesn't need to search anywhere; it just goes straight to that specific spot on your hard drive to execute the file.

However, when you type just the command name (hello.sh), the computer behaves differently:

1. The Computer is "Lazy"
The computer doesn't look everywhere on your hard drive for a command (that would be extremely slow). Instead, it only looks inside the specific folders listed in your PATH variable.

2. The Verification Gap
If you type hello.sh and get "command not found," it means the PATH variable does not currently contain the directory where that file lives.

Think of the PATH like a list of bookshelves your computer is allowed to check. If your script is on a bookshelf in the garage (~/my_scripts), but the PATH only tells the computer to check the living room and kitchen, the computer will effectively say, "I can't find it," even if the file is physically right there in the garage.

Why the Direct Path bypasses this:
When you provide the direct path, you are essentially "handing" the file to the computer and saying, "Run this specific file." You are bypassing the search process entirely.

How to fix it so you don't have to use the direct path:
To make it work by just typing hello.sh, you must ensure two things happen in the same terminal session:

The directory must be in your PATH:
Run echo $PATH. If you don't see /home/labex/my_scripts in the output, the computer doesn't know to check that folder. Run the export command again to add it.
The folder must be listed correctly:
Double-check for typos. If the directory is named my_script but you added my_scripts to the path, it won't work.
Pro-tip: You can confirm if the computer is currently "looking" in your folder by running:
ls $PATH | grep "my_scripts"

If that returns nothing, the shell isn't looking in your custom directory, which is why it forces you to use the full/direct path every time!
