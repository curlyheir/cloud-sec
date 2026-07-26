GitHub SSH Setup on Ubuntu

objective

Configure secure SSH authentication between Ubuntu and GitHub to eliminate password and token prompts when pushing code.

Tasks completed

1. Generated an ED25519 SSH key pair on Ubuntu

2. Started the SSH agent and added the private key

3. Added the public key on GitHub

4. Verified GitHub SSH authentication

5. Changed the repository remote from HTTPS to SSH

6. Tested repository access and Git operations.

# Commands Used

- ssh-keygen

- ssh-add

- ssh -T git@github.com

- git remote set url origin

- git push origin main

- git pull --rebase origin main

# Lessons Learned

1. GitHub no longer supports password authentication for GIt operations over HTTPS.

2. SSH provides a secure and convenient authentication method.

3. Git repos can be migrated from HTTPS to SSH without recreating the repository.

4. Branch sync issues can occur when local and remote histories differ.

# Outcome

- successfully configured SSH authentication between Ubuntu and GitHub and gained hands-on experience with Git, GitHub, Linux command-line operations, and repository management.

