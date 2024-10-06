### Create a new dotfiles repository:
1. `mkdir $(pwd)/.mcs`  
2. `git init --bare $(pwd)/.mcs`  
3. `echo "alias mcs='/usr/bin/git --git-dir=$(pwd)/.mcs/ --work-tree=$(pwd)'" >> $HOME/.bashrc`  
4. `bash`  
5. `mcs config --local status.showUntrackedFiles no`  
6. create a new repository on GitHub *(or any other Git server hosting service)* but do **NOT** include a `README.md` or any other files such as a license  
7. `mcs remote add origin https://github.com/<username>/<repository_name>.git`  

***

### Clone *(download)* a Minecraft server dotfiles repository:
1. `echo "alias mcs='/usr/bin/git --git-dir=$(pwd)/.mcs/ --work-tree=$(pwd)'" >> $HOME/.bashrc`  
2. `echo '.mcs' >> .gitignore`  
3a. `git clone --bare https://github.com/<username>/<repository_name>.git $(pwd)/.mcs` *(general Minecraft server dotfiles repository)*  
3b. `git clone --bare https://github.com/zahradnik-ondrej/mcs.git $(pwd)/.mcs` *(this Minecraft server dotfiles repository)*
4. `bash`
5. `mcs checkout -f`  
6. `mcs config --local status.showUntrackedFiles no`
7. `bash`
