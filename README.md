git_purge is a simple bash script meant to clean git config files to ensure
that traces of previous users who may or may not have used git on your computer
are completely removed. 

(Shame on them for not removing themselves better.)

This short script gives the user 5 options to use. 

Basic Clean: Removes the user.name and user.email from .gitconfig as well as 
unsetting the password cache using commands built into git.

Heavy Purge: Locates the user's .gitconfig file, and destroys it. Afterwards, the
file is recreated to ensure there are no dependency errors. 

SSH Clean: Destroys all possible RSA keys likely associated with a git account.
Because of the impossibility of knowing which keys belong to git, it is 
recommended that the user run these commands manually. However, if truly
wanted, the script will take its best guess.

Set Credentials: Quickly set/overwrite global user.name and user.email without
typing the entire git config --global etc.

Intensive Search: Finds all files



To run:

```
chmod a+x git_purge
./git_purge
```