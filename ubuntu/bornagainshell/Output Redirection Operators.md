## Output Redirection Operators

[ Before a command is executed, its input and output may be redirected using a special notation interpreted by the shell ]

Redirection operators in Linux are shell symbols that alter the default source of input or destination of output for commands, controlling/altering how data flows between the terminal, files, and other processes.

By default, commands read from [ standard input (stdin/0) (keyboard), ] send normal results to [ standard output (stdout/1) (screen), ] and send errors to  [ standard error (stderr/2) (screen) ]

>: Redirects stdout to a file, overwriting its existing content. 

>>: Redirects stdout to a file, appending to the end without deleting current data. 

<: Redirects stdin from a file, allowing a command to read input from a file instead of the keyboard. 

2>: Redirects stderr to a file, capturing error messages separately. 

&> or > file 2>&1: Redirects both stdout and stderr to the same file. 

|: The pipe operator passes the stdout of one command as the stdin to another command.

1. Before a command is executed, its input and output may be redirected using a special notation interpreted by the shell. Redirection allows commands’ file handles to be duplicated, opened, closed, made to refer to different files, and can change the files the command reads from and writes to. 

2. When used with the exec builtin, redirections modify file handles in the current shell execution environment. The following redirection operators may precede or appear anywhere within a simple command or may follow a command. Redirections are processed in the order they appear, from left to right.
