# how to use this git repository

* the repo is separated into 3 sub modules
    1. engn1650-3Dpen-mcu
    2. engn1650-3Dpen-pc
    3. engn1650-3Dpen-app

* this is a useful link about submodules in git https://git-scm.com/book/en/v2/Git-Tools-Submodules
* all instructions assume you have the ssh key set up and connected to your github. If not, follow https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent or use Github Desktop if preferred. 

* To set up and use the repos, follow these instructions:
    1. Make a local top level directory or navigate to the directory where you want your files to live 
        e.g. mkdir ~/Documents/engn1650
        e.g. cd ~/Documents/engn1650

    2. In the shell, clone engn1650-3D pen into your directory. This is the top level repo.
        git clone git@github.com:jluke1764/engn1650-3Dpen.git

    3. The directories for the subrepositories will be there, but may be empty. To clone the sub repos, run 
        git submodule update --init --recusive

    4. if you want to push changes, make sure you are in the correct directory in the terminal. Run git status to see what files have changed. 
    
    5. Add the desired files using git add <filename>

    6. Run git commit -m '<message about the changes you made>' 

    7. Run git push to fully update your changes to the repo

    8. The higher level repos will still be pointing towards an older version of the sub module. If you go up to the next repo and run git status, you should see that the directory with the submodule is different. Then do git add, git commit, and git push to fully update.

* 

# useful git commands
* git status
* git log
* git branch
* git add
* git commit -m
* git push
* git pull
* git <command> --help
* git diff
