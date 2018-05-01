# CSCE-31 Teaching Tips - Cheat Sheet for Assignments

 There are many development tools required to use and many precedures to perform in order to set up certain environments to do your assignments in this course.  Creating simple cheatsheets for tools and setup prececures can help save time doing assignments which I felt was more time consumming than I expected.  This document **_does not cover the initial set ups_** that only require to be done once. You need to look at the set up procedures provided in the class. It **_only covers the precedures you need to repeat_** for the assignments.

  I was not familiar with github and commnand line commands.  We had assignments due once in two weeks and when I was away for 10 days doing other work and come back, I forgot all about the development procedures and environments and had to look up videos from the week 1 and week 2. When I have to deploy the working solution to Digital Ocean, I had to look through the course video again to find out what I need to do.  So, this cheatsheet is to reduce time looking for procedures and commands.


## Step 1: local working directory setup
- Click on the link from the assignment page that will create a github repository for you to use.
- Open a terminal window and create or go to your local working directory
```
$ cd /your/local/directory
or
$ mkdir yourdir
$ cd yourdir
```
- connect to github from terminal
```
$ ssh -T git@github.com
```
- go to your github repositories site and select the repository for the assignment
- select the green button with 'Clone or download', copy the https path of the repository, go back to terminal to clone the repository to your local hard disk.
```
$ git clone [your repository url copied]
eg) $ git clone https://github.com/HarvardDCENode/assignment-6-angular-jaechong.git
```
## Step 2: using node module packages, Express Generator, Angular
- For all assignments or projects, make sure to create a package.json first to manage node modules
```
$ npm init
```
- To use Express
```
$ npm install --save express
```
- For development, update package.json to add "start-dev" to automatically restart the server when the code changes.
```
  "scripts": {
    "start": "node ./bin/www",
    "start-dev": "nodemon --inspect ./bin/www"
    },
```
- to run your Web Server,
```
$ npm run start
or 
$ npm run start-dev
```
- To use Express Generator to prepare all the packages and 
```
$ sudo npm install -g <directory_name>
```
- To use pug templates
```
$ express --view=pug <myapp_name>
```
- Testing your app on your browser on port 8080
```
http://localhost:8080
```
## Step 3: saving your work to Github repository
- Once your code is working locally or you just want to save the code to github, open your terminal and connect to github
```
$ ssh -T git@github.com
$ cd /your/local/directory
```
- make sure that you update .gitignore file to include files you should not submit to github
```
$ nano .gitignore
```
- to check what files have been updated
```
$ git status
```
- to add your code to stage commit
```
$ git add .
or
$ git add --all
```
- to commit your local changes
```
$ git commit -m "description of your commit"
```
- to push all your changes to your github repository
```
$ git push origin master
```
## Step 4: deploying to Digital Ocean
- Write down you D.O IP Address here : ___ . ___ . ___ . ___
- SSH to D.O.
```
$ ssh root@<your ip address>
```
- SSH Keys between the server and github must be setup already.
- Test your connection from the droplet:
```
$ ssh -T git@github.com
```
- clone your code from github to DO
```
$ git clone https://github.com/assignment-1-getting-your-environment-set-up.git
```
- Navigate to your directory, in this example, assignment-1-getting-your-environment-set-up
```
$ cd assignment-1-getting-your-environment-set-up.git
```
- construct node modules using package.json
```
$ npm install
```
- test your app running on DO, first check if any process is running
- To kill the process
- First find the node process
```
$ ps aux | grep node
```
- use 'kill' to kill the node process
```
$ kill <process number>
```
- start the server on DO
```
$ node bin/www
```
- to run the server continuosly even when the terminal window closes, run this
```
nohup node bin/www &
```

## commands for Mac Terminal
 input  | results
 --------------- | ----------------------------------------------- 
 Tab             | Auto-complete files and folder names 
 Ctrl + C        | Kill whatever you are running        
 Ctrl + D        | Exit the current shell               
 cd ~            | Home directory, e.g. 'cd ~/folder/'         
 cd /            | Root of drive                               
 ls              | Short listing                               
 ls -l           | Long listing                                
 ls -a           | Listing incl. hidden files                  
 ls -lh          | Long listing with Human readable file sizes 
 ls -R           | Entire content of folder recursively        
 touch [file]    | Create new file                             
 nano [file]     | Opens the Terminal it's editor              
 pwd             | Full path to working directory 
 cat             | Concatenate to screen 
 rm [file]       | Remove a file, e.g. rm [file] [file]
 rm -i [file]    | Remove with confirmation
 rm -r [dir]     | Remove a directory and contents
 rm -f [file]    | Force removal without confirmation
 cp [old] [new]  | Copy file to file
 cp [file] [dir] | Copy file to directory
 mv [old] [new]  | Move/Rename, e.g. mv -v [file] [dir]
 mkdir [dir]     | Create new directory
 rmdir [dir]     | Remove directory ( only operates on empty directories )
 rm -R [dir]     | Remove directory and contents 
 > [file]        | Push output to file, keep in mind it will get overwritten 
 >> [file]       | Append output to existing file 
 <               | Tell command to read content from a file 
 [command] -h | Offers help 
 clear           | Clears the terminal display
