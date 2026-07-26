## Modifying Users

# useradd

''' bash
useradd greenknight
''
The command [ useradd ] adds user to system environment.

# checking user info

''' bash
grep -w greenray /etc/passwd
'''

[grep] command-line tool used for searching text. It scans through a file or input for lines that match a specific pattern and then displays those lines.

the flag [ -w ] ensures that grep finds the exact whole word specified.

[ username ] - user specified in the search command to look for these defined usernames in the [ user database ].

[ /etc/passed ] is a central database that stores essential info about all registered users on the system : username, userid, home dir, & default shell.

# Output

'''bash
greenray:x:1000:1000:greenknight:/home/greenray:/bin/bash
'''
- Username - greenray
- x - paswword placeholder
- 1000 - user id - uid
- 1000 - group id - gid
- home dir - /home/greenray
- Default shell - bin/bash

# System logic

- The system reads this file for the identiy of a user every time they log in or interact with the system.

- Who are you? [ username ] Where is your home? [ home dir ] What language should I communicate to you in? [ shell ].
