# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> >  CHEAT SHEET  
* ```pwd``` show current working directory path  
* ```mkdir``` create a directory  
* ```rmdir``` delete an empty directory or ```rm -rf <directory>``` to delete a non-empty directory   
* ```touch <filename>``` createss file using ```touch``` command  
* ```rm <filename>``` delete a file  
* ```mv <filename> <newpath>``` renaming a file  
* ```cp <orig-path\filename> <new-path>``` copy a file from one directory to another  
* ```man <command>``` get manual pages for specified command
* ```history``` get command line history  
 
---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

> > ls options  
`ls` lists non-hidden (ie. files that don't begin with a dot) items in a directory  
`ls -a` includes hidden directory entries  
`ls -l` displays directory entries in long format  
`ls -lh` uses unit suffixes for directory entry sizes when displaying in long format  
`ls -lah` same as -lh but including hidden entries  
`ls -t` sorts directory entries by time last modified  
`ls -Glp` colorizes long format results and adds a `/` at the end of entries that are themselves directories  

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> >  more `ls` options  
`ls -R` lists files recursively in subfolders  
`ls -1` lists files one row per file  
`ls -laSh` lists files in size order (with size suffixes)  
`ls -F` like -p adds symbols to certain special file types  
`ls -ul` lists time of last access (can also be used in conjunction with -t for time-based sortin)  

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > the xargs command line utility allows for the easy and customized building of argument lists that can be passed into other command line utilities (particularly those that may not accept argument lists).  an example of playing all mp3 files in a directory can be given by:  
`$ find . -iname "*.mp3" -print | xargs -0 -I mp3file mplayer mp3file`

 

