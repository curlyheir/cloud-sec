# linux pipes

In Linux, a pipe [represented by the | symbol] [ is a fundamental mechanism for inter-process communication that connects the standard output (stdout) of one command directly to the standard input (stdin) of another. ] 

[This unidirectional channel] allows processes to chain together, enabling the output of the first command to serve as the immediate input for the next without storing data in temporary files.

The basic syntax follows the pattern command1 | command2, where data flows from left to right. For example, 

'''bash
ls | grep "file.txt" 
'''

lists directory contents and filters them for specific strings in a single, efficient workflow. 

'''bash
cat /etc/group | sort
'''
output :
        cat opens /etc/group and reads every line in it, then instead of printing a long list the pipe | catches the data it reads and holds it, sort - receives the data from the pipe | & rearranges it from A to Z, then prints the organized result to the terminal.
