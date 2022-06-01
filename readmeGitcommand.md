# CREATING A GIT REPOSITORY & PUSHING FILES ON GIT HUB
## Create a repository
- Open the terminal and type the command ```pwd```. which will show your working directory.
- Type this command > ```ls``` which will provide the list of the files you have in your directory or echo "# patricia-notes" >> README.md. 
- Type the ```git init``` command to enter the files available  in your directory.
- Then we change the branch from _master_ to _main_ by using the ```git branch -m main``` command. 
- Add the ```git add``` command then add the name of the file you are entering like for example ```git add readmeGitcommand.md``` which will  stage the files to the repository from the folder. 
- Then type the ```git status``` command to see all the file you have staged in the repository.
- Commit the files you had staged by using the `git commit -m “notes on pbx”` command.
- Then copy the remote url it can either be ****https** or ****shh** on the repository created then, type the following command ```git remote add origin git@github.com:darwinist-ou/patricia-notes.git```  paste the url provided from git.
- After that, push the  repository by using the following command ```git push -u origin main```.
- Then enter your user name and password. check the repository to see how your files have been pushed.
 ### GIT CLONE 
 - clone downloads an existing Git repository to your local computer in the directory created.The following command is used to clone ```git clone url```a repository from an existing one. This is how the command should be after entering the url ```git clone https://github.com/hd-David/camera.git``` and press enter or return on your key-board.
- When you use the ```ls -la ```command, it will show or give a list of files that exists in cloned repository where the folder is located.
- After this is done you can use the ```cat``` command and the name of the file you want to open. This is how the command should be after entering the name ```cat readme.md```,once done it will show what that file contains.

