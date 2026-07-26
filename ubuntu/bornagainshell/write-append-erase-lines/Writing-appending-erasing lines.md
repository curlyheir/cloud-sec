## Writing & erasing lines with Redirectional Operators

There are more than one way to write onto a file, in this case i was using the command [echo] 

'''bash
echo "i brokeshell guess im bornagain" > beagainshell.txt
'''

this redirectional operator [>] allowed me to write this initial line on to the .txt file.

'''bash
echo " need some vertical space to break wind " >> beagainshell.txt
'''

the redirectional operator [>>] allowed me to add a new line to the file, and not overwrite it.

'''bash
cat beagainshell.txt
'''

output: i brokeshell guess im bornagain
        need some vertical space to break wind

I used [cat] to check the content in the file to make sure that the command went through or if i made a mistake in the command line.

# sed

[sed] (Stream Editor) is a non-interactive stream editor in Linux/Unix [used to filter and transform text from files or pipelines.]  It processes input line-by-line, performing basic text transformations such as [searching, replacing, inserting, and deleting strings] without requiring an interactive interface. 

'''bash
sed -i '4s/.*/need me some vertical space to break wind/' BornAgainSheLL.txt
'''

'''bash
sed -i '2s/.*/i brokeshell guess im bornagain/' BornAgainSheLL.txt
'''

with [sed] i was able to edit the txt file,
flag [-i] edits the file in place (modifies the original file directly)
[4] targets only line 4

[ s/.*/text here/ ]
This  substitute command where  [.*] matches any character sequence on that line, replacing that text with /text here/.


# Note 1
option [-i] allows me to search, replace, delete or insertions & save changes immediately without needing to redirect output a new file.

# using cat

cat << EOF > multiline.txt >
i am writing
this 
in 
a
simplified
way
EOF

# The System logic of above complex command

1. cat normally reads file contents, but combined with operaters it [gathers input]
2. << operator allows you to type multiple lines of text; sys stores in memory
3. inputing OEF on the last line, the sys recognizes this as the stopping point
4. > operator triggers the save process

'''bash
nl multiline.txt
'''

[ nl ] adds line numbers to the output which is helpful for referencing specific lines.
[ head -n 2 multiline.txt ] or [head -n2 multiline.txt] head displays the start of a file, while [ -n2 or -n 2 ] shows the 1st two lines.
[ tail -n 1 multiline.txt ] or [ tail -n1 multiline.txt ] tail displays end of a file. [ -n1 or -n 1 ] shows the last line of the file.

nano multiline.txt 

text editor

exit nano text editor [ ctrl + x + y, then enter ]
