# reading-notes
The Terminal Line 
-What is it ?

Command line is a text based interface to the system , you can deal with by typing commands on keyboard and the feedback will return as atext also .

-How do i get to one ?
To get to terminal that depends on every system .
If yoy are using Mac you will find it in Terminal under Applications->Utilities. 
I you are using Linux then Applications->System or Application->Utilities .
I you are using Windows and you want to get remotly into another machine you will need an SSH.

-How does it work ?
Command line will present you with prompt whate you are typing will display after prompt such as (user@bash) its a prompt after the prompt enter your command , and then you have what are reffered to as acommand arguments .
##bash its acommon type of SHELL ,shell is a part of operating system that defines how your terminal will behave after executing , there are several types of shells such as (zsh) , to know which shell you are using use echo command such (echo$SHELL).

-Basic Navigation

Many tasks rely on being able to get to or reference the correct location for a file or your directory these are important stuff to be able to work effectively in Linux.

-how to get around it
#pwd
To know your current location or present working directory , you can determine the location by run  pwd command (Prtint Working Directory).
There is two types of path , using either type the system will direct you to the same location.
1.Relative path :the location relative to where currently the file in the system
2.Absolute path :location relatid to the root of the file system .
#cd 
In odrder to move around the systemuse (cd) command which stand for change directory and move between directories
#ls
Some times you want to know and check your directory contents you can use ls for that purpose .

-More About Files
Every thing is actuall a file text is a file ,keyboard ,directory and monitor all of these are files . A fle extension normally a set of 2-4 characters after full stop at the end of a file (.exe , .txt ,.png ) .
Linux is extensionless system so files can have any extension or non at allsince it ignores the extensions and look inside the file to determine what is the type of the file , (file[path]) command can use to find this out. 
--Some characteristics of files 
#Linux is Case Sensitive 
if uou have two or more files with the same name but letters are different ypu have to be carfull about the case (file.txt , File.txt) are adifferent files .
Also in commands you have to be aware abot sensetivity (ls ,lS) differnt commands
#Spaces in Names 
Be carefull with spaces , if you want to move nto directory (My photos) it containes spaces so lets say (cd My photos) it will be seen as two commands ,two ways to go about this.
##Quots (Single or Double quots) 
Any thing inside quots considerd as one item ("My photos").
##Escape Characters(\)
Backslash just escape the special meanings for next character(My\ photos).
#Hidden Files and Directories 
Files may be hiddden for specific reasons configraton files or particular user ,no special commands to make file hidden ,if the file begins with a.  then it considerd to be hidden ,and you may rename your file to remove the . and it becomes unhidden .
The command ls -a wll show for you lst of contents including all hidden files or directoies.

-Manual Pages
Manual pages are your friend explain every command includiing what they do ,to invoke the manual pages with the following command (man<your command>) to exit the man pages press 'q' for quit.
Commands have long andd short hand version , long hand more human readdable form andd it can be easier to remember what commands are doing ,short hand you can chain multiple together easier  but both do the same thing .
long hand command begin with two dashes (--) but shorh hand begins with(-) by using single dashes yo unvoke several options by placing all the letters representing options together after dash.
##Searching
If you are not sure of what command you may use and you know what yo want to achieve do a keyword search all manual pages containing the given search item(man -k <search term>) 

-File Manipulation 
Linux organize file system in heirarchial way ,so its usefull to organaize stuff an elegant file structure .
##Creating directory is easy by run (mkdir <your directoy name>) and it will create for us .
To create blank file which is a file that has a nice features by using this command (touch<filename>)
##Removing directory it also easy ,one thing you have to be carefull about  however  that there is no undo when it comes to the command line on Linux 
No undo means linux command doesnt have an undo feature , perform destructive actions carefully. The command to remove directory is (rmdir<your directory name>).
For removing a file (and non empty Directories) the command to remove or delete is (rm).
Removing non empty directories 
when rm is run with the -r option it allows us sto remove directories and all files and directories contained within .
Always we can check the manual pages to see what rm has options to do since Most commands have many useful command line options make sure to skim man pages for new commands to be familiar what they can do.
##Copying a File or Directory
Some times you want to make a duplicate of a file or directory by using cp command .(cp <source><destination>)
##Moving a File or Directory .
We use this command (mv<source> <destination>) , source and destination are paths what ever its relative or abssolute paths .
##Renaming Files Or Directory 
Normally mv will be used to move files into a new directory so we may provide a new name for the file or directory and as ppart of moving it also will rename it .

###Cheat Sheat
Basic Navigaton 
pwd : Where am i in the system
ls  :perform a listing of the given path or our current directory 
- common options -l ,-h ,-a
cd  :Change into the given path .
path :Adescription of where a file or directory is on the filesystem .
Absolute path :One beginning from the root of the file system 
Relative path :One relative to where you currently are in the system
~(tilda) :used in paths as a reference to your home directory 
.(dot):Used iin paths as a reference to your currrnet directory 
..(dot dot): Used n paths as a reference to your current directories parent directories.
TAB completion :Start typing and press TAB . the system will auto complete the path ,TAB twice it will show you your alternatives.

-More About  Files
file [path]:Find out what type of item a file or directory is.
Spaces in Names :ut whole path in quots or backslash in front of spaces.
Hidden Files Or Directories : A name beginning with a. 

-Manual Pages 
man <command>:View the man pafe for a command
man -k<search item> :Search for man pages containning the search term.
**press q to exit amn pages.

-File Manipulation
mkdir<directory name>:Create a directory.
rmdir<directory name>:Remove directory(only if empty).
touch<file name> :Creat a blanck file.
cp<source><destination>: Move the source file destinnation ,May also use to Rename files or directory.
rm<path>:Remove a file or ditrectory ,Common options :-r  -f










