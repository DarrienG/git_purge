git_purge is a simple bash script meant to clean git config files to ensure
that traces of previous users who may or may not have used git on your computer
are completely removed. 

(Shame on them for not removing themselves better.)

This script cleans in three phases, and prompts the user at each phase with a 
short description of what will happen at each one. 

Phase 1: Removes the user.name and user.email from .gitconfig using commands 
built into git.

Phase 2: Locates the user's .gitconfig file, and destroys it. Afterwards, the
file is recreated to ensure there are no dependency errors.

Phase 3: Destroys all possible .ssh keys likely associated with a git account.
Because of the impossibility of knowing which keys belong to git, it is 
recommended that the user run these commands manually. However, if truly
wanted, the script will take its best guess.

To run:

```
chmod a+x git_purge
./git_purge
```