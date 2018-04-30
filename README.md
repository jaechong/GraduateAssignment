# Graduate Assignment
# CSCE-31 Teaching Tips

The following two topics tips should help the students taking CSCI-E31 course:
- Create Assignments Cheatsheets
- Emphasizing I would like to discuss the things that I struggled or made me spend more time than I should.  I believe teaching these will help students taking CSCE-31 course.
1. There are many development tools required to use and many precedures to perform in order to set up certain environments to do your assignments in this course.  Creating simple cheatsheets for tools and setup prececures can help save time doing assignments which I felt was more time consumming than I expected.
2. There are also many new templates/languages, packages, and frameworks learned in this course.  Certain topics or concepts which could be discussed in 
### Assignments Cheatsheets
### Topics that caused 

# PART 1 : Cheat Sheet for Assignments
  I was not familiar with github and commnand line commands.  We had assignments were due once in two weeks and when I was away for 10 days doing other work and come back, I forgot all about the development procedures and environments and had to look up videos from week 1 and week 2.


## Step 1: local working directory setup
- Click on the link from the assignment page that will create a github repository for you to use.
- Open a terminal window and create your local working directory
```
$ cd /your/local/directory
ssh -T git@github.com
```
- go to your github repositories and select the repository for the assignment
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
- For development, update package.json to add "start-dev" to automatically refresh your site when the code changes.
```
  "scripts": {
    "start": "node ./bin/www",
    "start-dev": "nodemon --inspect ./bin/www"
    },
```
- Then execute,
```
$ npm run start
or 
$ npm run start-dev
```
- To use Express Generator to prepare all the packages and 
- 
- Using 
## Step 3: saving your work to Github repository

## Step 3: deploying to Digital Ocean

## commands for Mac Terminal
 input           | results
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
 <               | Tell command to read content from a fi 
 [command] -h | Offers help 
 clear           | Clears the terminal display

Developement Setup:
  - local developement environment
  - debugging
  - Digital Ocean and production environment

Critical Concepts:
  - Import and save files from GitHub, Dropbox, Google Drive and One Drive
  - Drag and drop markdown and HTML files into Dillinger
  - Export documents as Markdown, HTML and PDF
