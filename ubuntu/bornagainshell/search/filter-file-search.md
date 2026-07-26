# apropos 

the [apropos] command helps you find commands related to a specific keyword. This
is useful when you know what you want to do but you're not sure which command to use.

'''bash
apropos file
'''

This command searches through the manual page descriptions for keyword "file" and (prints) a list of every command related to it. long list though..

'''bash
apropos file | grep create
'''

this will only show commands related to "file" that also mention "create" in their description of use.

# The components 

[ | ] [The Pipe] this is a powerful [connector]. it takes the entire list of results produced by the initial command on the left [apropos file] & sends it directly as input to the command on the fight [grep create]. 

[grep create] this command [filters] text. It searches through the stream of data it received (the list of 'file' related commands) and only displays the lines that contain the word "create".

# Overall System Logic

- The command acts like a specified filter:

1. we asked system "show me everything related to files"
2. then we applied a secondary pass(filter) "from that list, only show me the ones that also involve creating" 

- instead of scrolling through a huge list.

# less

'''bash
less beagainshell.txt
'''

- 
[less] - display the contents of a file in a terminal

# find
 
 '''bash
 find . -name "*.txt"
 '''
 
 find : search files and directories
 
[ . ]  tells [ search ] to start in the current directory
 
[ -name ] flag tells [ find ] to search based on a [ file name ] 
 
 [ "*.txt" ] this is the pattern find is searching for
 
[ * ] is a wildcard that represents any characters
 
find any file that ends with [ .txt ] 
 
 - Globbing is a pattern-matching technique used in computing to match and expand filenames or paths using wildcard characters rather than specifying exact names.
 
 - Originating from the Unix command glob (short for "global"), it allows users to efficiently select multiple files that fit specific criteria, such as using an asterisk (*) to match any number of characters or a question mark (?) to match a single character.
 
 '''bash
 find ~ -size +1M
 '''
 [ ~ ] this starts search in home dir
 
[ -size ] this flag tells find to filter search based on [ file's size ]

[ +1M ] this portion defines measurement
[ 1M ] stands for [ 1 Megabyte ] 
[ + ] means [ greater than ]

- search home dir beased on file sizes greater than 1 megabyte.

- This is a very helpful command when you are trying to free up space, as it quickly highlights which files might be taking up a significant amount of room in your storage.


'''bash
find ~ -mtime -1
'''

[ ~ ] home dir 

[ -mtime ] this flag stands for [ modification time ] 

[ -1 ] this specifies [ time window ]

[ - ] this minus sign is [ less than ] 

[ 1 ] this represents [ one 24-hour period ] 

# which

'''bash
which bash
'''

[ which ] is a search tool that searching system's [PATH]. The Path is a predifined list of dirs that your computer checks whenever you tell it to run a prog.

If it finds a file named bash that is marked as executable,[it stops searching]and displays the full path to that file on your screen [ /usr/bin/bash ]

If it doesn't find the program, it simply won't return anything.
