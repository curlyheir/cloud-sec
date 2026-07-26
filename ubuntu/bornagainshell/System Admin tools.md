## checking system info

[ uname ] : check operating system info. flag [ -a ] displays all system info.

[ who ] : who else is working on dev server

[ id ] : inspect usergroup, group members for proper access control

[ top ] : to monitor system processes & resource usage to ensure optimal performance

[ > and >> ] : to document info in professional reports.

[ uptime ] : show measures of system reliability in terms of system load averages.

# writing system report from shell

[ output redirection operators > and >> ] are used to write the command outputs into the specified file.

'''bash
whoami > system_report.txt : user & permissions 
'''

- this command writes the current user and permissions onto the system_report.txt file.

'''bash
uname -a >> system_report.txt 
'''

- this writes all system info on the file.

'''bash
uptime >> system_report.txt : uptime measure
'''

- this writes the uptime info onto the file.

'''bash
uptime -p >> system_report.txt : human-readable duration

'''
- this writes a more human-readable report onto the file.

'''bash
uptime -s >> system_report.txt : start time
'''

- this writes the start time onto the file.

'''bash
cat system_report.txt 
'''

- this reads the file we just printed all of this info on. 

# note

- Linux [ output redirection operators ] are shell symbols that alter the default source of input or destination of output for commands, controlling/altering how data flows, [ allowing data to be directed to files, other commands, or devices ]


