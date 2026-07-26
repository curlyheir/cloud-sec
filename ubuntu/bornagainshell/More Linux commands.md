## More Linux commands

# tar

'''bash
tar -xf archive.tar -C /path/to/new/directory
'''

This command saves many files together into a single tape or disk archive, and can
restore individual files from the archive.

# useful flags with tar

-x: Extract files from the archive. 
-f: Specify the archive filename. 
-C: Change to the specified directory before extracting. The target directory must already exist; tar will not create it automatically. 

# remember
- tar does not automatically create a [destination directory] before extracting files from archive. You should already create the destination directory before the [tar] command, then use flag [-C] to specified the destination. 

# clear

'''bash
clear
'''

[ clear ] will clear text previously printed in your terminal, but won’t delete anything (scroll up to see old output again).

# grep

'''bash
grep -r "find this fine voice" .
'''

this command [ grep ] w/ flag [ -r ] will search for the words " find this fine voice" in files that can be reached from current directory. 
