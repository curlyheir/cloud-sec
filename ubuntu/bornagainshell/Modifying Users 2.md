## Modifying Users 2

# setting password for a user

'''bash
sudo passwd greenshield
'''

This will set a password for the user.

# checking 

'''bash
sudo passwd -S greenshield
'''
- output : greenshield P 06/02/2026 0 99999 7 -1

# System logic

- greenshield - username being checked
- [ P ] password set [ L ] account locked [ NP ] no password
- [ 06/02/2026 ] the date when the password was last changed
- [ 0 ] (minimum age) the number of days a user must wait before they are allowed to change their password again
- [ 99999 ] (maximum age) the number of days the password is valid before it expires and forces a change 
- [ 7 ] (warning days) the number of days before password expiration. 
- [ -1 ] # of days after password expires, to the account being disabled. [ -1] [ usually means that this feature is turned off ]

