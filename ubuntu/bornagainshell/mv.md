## mv 

# move and renaming in one command.

'''bash
newdir/oldname.txt ./newname.txt
'''

[ mv ] this command tells system to either [ move ] or [ rename ] an item.

newdir/oldname.txt : this [ source path ] tells computer to look inside [ dir ] named [ newdir ] to find the file named [ oldname.txt ]

./newname.txt : [ destination path ] 

[ ./ ] this is your [ current dir ] 

[ newname.txt ] this is the newname

## System Logic

[ mv ] takes [ oldname.txt ] out of the directory [ newdir ]
[ reanames ] it to [ newname.txt ] and places the file directly into
your current folder.

# more mv

'''bash
mv greenote.txt ..
'''

[mv] moves & [ .. ] is the parent directory [ one level up ].
