## Linux flags

These are known as options or switches, that modify the behavior (parameters) of the command line. 

Purpose: Flags allow users to customize output formats, enable recursive operations, enforce verbose logging, or interact with the command, providing flexibility without needing separate commands for every variation. 

SIMPLIFICATION**

'''bash
ls -l
'''

[ -l ] (lowercase l) "long" format listing. You'll see additional details like file permissions, owner, size, and modification date.

[ flags ] modify the command

Syntax: The general structure is command [flags] [arguments], such as ls -la to list all files in long format.

'''bash
ls -la
'''

[ Combination Flags ] Short flags can often be grouped together after a single hyphen

'''bash
ls -a
'''

This flag [ -a ] will show all files including dot . hidden files.

'''bash
grep --help
'''

This flag [ --help ] displays help text or usage information for a program & then exit.


#note
ls -la is equivalent to ls -l -a 

