# ComposeUtil
Utility to deal with Docker Compose stacks in a fixed directory, ✨With simplicity✨.  
This program needs docker/podman and a compose plugin, obviously.  
Started as a few bash aliases for personal use, then turned into a script, and ended up here.

# Installation
Simply:
* Download the script,
* Open it in a text editor of choice,
* Edit the top three variables:
   ```bash
   # Directory where all of your stacks are located. (NO TRAILING SLASH)
   BASEDIR=/opt/stacks
   
   # Name of your compose files
   FILE=compose.yml

   # Container Engine name (docker, podman, etc.) (NOT podman-compose or docker-compose, etc.)
   CTRNAME=docker
   ```
* Place the script in a directory that's within `PATH`,   
... And you're done!

# Compatibility
This program has been tested with `docker` and should work with `podman` aswell, however other engines have not been tested, but may work.   

# Usage
This program is basically compatible with all of `docker-compose`'s commands, plus a few extras:
```
Special commands (marked with '*' means does not need stack-name):
  *cd Starts a new shell in the directory of the stacks
  *ls Shows all available stacks.
  mod Modifies the existing stack or creates a new one.
```
The program Terminates with exit code 128 for syntax errors, passes through error-codes of the engine otherwise.
