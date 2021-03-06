# terminal-commands

<br><br>

To install cocoapods in global level
====> sudo gem install cocoapods
<br><br>

To install cocoapods in global level at specific version
====> sudo gem install cocoapods -v 1.10.2
<br><br>

To uninstall cocoapods in global level
====> sudo gem uninstall cocoapods
<br><br>

To check the version of cocoapods installed the current machine or macbook
====> pod --version
<br><br>

Question:
To get back to down version of cocoapods the required steps is as below
<br><br>

Step 1 - uninstall cocoapods using the command ====> sudo gem uninstall cocoapods
<br><br>

Step 2 - make sure the pod directory is removed in the machine using the command ====> pod --version ===> it will give response like folder is not found
<br><br>

Step 3 - so now install the down version by using the command ====> sudo gem install cocoapods -v 1.10.2
<br><br>

Step 4 - now check the version of cocoa pods with the command ====> pod --version
<br><br>

<br>
get swift version ===> swift --version
<br>
get ruby version ====> ruby -v
<br>
get pod version ===> pod --version
<br>
add fastlane file ===> fastlane init
<br>
add .gitignore file ===> touch .gitignore
<br>
add pod file ===> pod init
<br>

<br> Shell Script Basics

<br>
to get list of contents ===> ls
<br>
to get additional or more details of contents ===> ls -l -h
<br>
to get list with size as mentioned way ===> ls -l -h --block-size=MB ===> here block-size will be either KB or MB or GB or etc......
<br>

date ==> displays ssystem date and time 
<br>
whoami ===> displays who is logged as current user
<br>
--help ===> displays list of options to the given command
<br>
man ====> displays user manual for given command
<br>
clear ===> clears the shell
<br>
history ===> shows last five hundreads of commanmds
<br>
exit ====> ends the shell
<br>
<br>
<br>
Shell Script using on Files and Folders
<br>
<br>
touch <placeholder for file name> ===> creates an empty file
<br>
Eg: <br>
touch Sample.txt  
<br>  
cat Sample.txt ===> reads the content from that file
<br>
echo "Hello, World!" ===> used to print something on console window.  
<br>
write content into the file using ">" symbol ===> echo "Hello, World!" > Sample.txt
<br>
  mv Sample.txt Test.txt ===> it will used to rename file from source to destination.
  <br>
  cp src_file dest_file ===> cp Test.txt fun_text.txt ===> it copies content from source file to destination file.
  <br>
  rm Test.txt ===> removes file from that folder or directory
  <br>
  ls -a ===> get all files along with hidden files or folders also
  <br>
  . ===> single dot ===> represents the current directory
  .. ===> double dot ===> represents the parent directory
 <br>
  <br>
  <br>
  Working with Directories
  <br>
  <br>
  mkdir tutorials ===> like empty file on touch command, it will also creates an empty directory
  <br>
  pwd ===> gives the current working directory name
  <br>
  cd ./tutorial ===> used to change the current working directory 
  <br> ===> . means current directory and /tutorial means go to inside of tutorial directory of current directory
  <br>
  cd .. ===> change directory to parent directory from current directory
  <br>
  <br>
  File Paths:
  <br>
  1. Absolute Path ===> path from root folder to current file or folder
  <br>
  2. Relative Path ====> path from current directory to other file or folder
  <br>
  <br>
  <br>
  cd ~ ===> used to move to your home directory
  <br>
  cd  ===> also used to move to your home directory
  <br>
  cd / ===> used to move to root directory, but not your home directory. remember this point
  <br>
  difference between root directory and home directory?
  <br>
  home directory ===> created for every logged in used inside root directory
  <br>
  root directory ===> root directory is common for every logged in uses, by default it is same as "/"
  <br>
  mv src_folder dest_folder ===> rename directory
  <br>
  mv src_file dest_folder ===> used to move file to folder
  <br>
  cp src_file dest_folder ====> used to copy src file to destination folder
  <br>
  cp -r src_folder dest_folder ====> used to create a copy of folder
  <br>
  rm -r directory_name ===> removes the directory or folder
  <br>
  
  <br>
  nano filename ===> it opens file in command line interface
  <br>
  cnrl + O and enter ===> it shows how many lines writteen on that file
  <br>
  cntl + X ===> closes the file and returns to terminal window
  <br>
  
  <br>
  <br>
  Filtering and Output Redirection
  <br>
  <br>
  
  head -2 sentence.txt ===> by default it returns first 10 lines of file, but here we mention 2 so it written first 2 lines of file.
  <br>
  tail -3 sentence.txt ===> by default it returns last 10 lines of file, but here we mention 3 so it written last 3 lines of file. 
  <br>
  grep
  <br>
  wc sentence.txt ===> returns number of lines, numbeer of words, number of characters in that file.
  <br>
  
  <br>
  Pipiing ===> "|"
  <br>
  <br>
  by using piping(|) we can execute multiple commands.
  <br>
  cat sentence.txt | head -2 
  <br>
  ====> here cat command reads all content and head command now take as input and returns output as first 2 lines.
  <br>
  
  cat sentence.txt | head -6 | tail -1 
  <br>
  ===> cat return total content and then head filters to first 6 lines and on top that tail return last one line as output
  
  <br>
  cat sentence.txt  | grep "rain"
  <br>
  ===> cat return total content and on top that grep command search with the pattern of "rain".
  <br>
  ===> and return the lines which matched the grep command containing pattern.
  
  <br>
  cat sentence.txt  | grep "rain" | wc
  <br>
  ===> return total number lines matching the pattern finally.
  <br>
  
  cat sentence.txt  | grep "rain" | head -1
  <br>
  ===> return first line on total filterd lines
  <br>
 
  <br>
  question:
  <br>
  Get 10 to 15 lines which containes "rain" in "sentence.txt" file?
  <br>
  <br>
  ANSWER:
  <br>
  cat sentence.txt | head -15 | tail -5 | grep "rain"
  <br>
  ===> cat command gets total content of file and passed and input to head command  in piping
  <br>
  ===> head command picks first 15 lines from top on that content and passed as input to tail command in piping
  <br>
  ===> tail command picks on top of that last five lines from bottom and passed as input to grep command in piping
  <br>
  ===> now grep command matches the pattern "rain" with the given input and return as output which matches the pattern.
  <br>
  <br>
  
<br>
  Output redirection
  <br>
  <br>
  in piping the output is cascaded to next command
  <br>
  but here in output redirection, 
  <br>
  output of command redirecting to file using ">" 
  <br>
  symbol meaning we are writing command output into the file.
  <br>
  <br>
  sentence.txt | head -6 > learnings.txt
  <br>
  ===> here the output of head command is puting inside the learnings.txt file using ">" symbol.
  <br>
  <br>  
  <br>
  Compressing and Uncompressing
  <br>
  <br>
  tar -czvf my_collection.tar.gz videos sentence.txt
  <br>
  ===> compress the given files and folders and saves to new file as with given name, here it is "my_collections.tar.gz"
  <br>
  
  tar -xzvf my_collection.tar.gz -C collections
  <br>
  ===> to un compress we use the above command where extracted files saved under collection folder. 
  <br>
  ===>make sure that directory alredy exist.
  <br>
  
  zip -r my_collections3.zip sentence.txt videos
  <br>
  ===> used to compress the files and folders to given file name here it is "my_collections2"
  <br>
  unzip my_collections2.zip -d collection2
  <br>
  ===> used to unzip the zipped file
  <br>
  
  
  # React Commands From Terminal
  <br>
  npx create-react-app Some-App-Name ===> creates an app with the given name
  <br>
  npm start ===> to start server at port 3000 as a localhost machine
  <br>
  npm install Some-Third-Party-Package-Name --save 
  <br>
  ===> used to install third party package into our react app and also it adds dependency to package.json file.
  <br>
  <br>
  
  # Kill Local Host Servers related processes
  <br>
  sudo lsof -i :3000 ===> gives running processes Ids and remaiing details.
  <br>
  kill -9 Procee-Id ===> give the node running process ID, to kill the local host servers.
  <br>
