## Linux_basic_command_for_beginners
#### vim
  * create file and open/edit
#### touch
  * create empty file
#### (esc; shift-colon) wq
  * save file
#### wq!
  * force
#### cat 
  * read the content
#### su
  * change user
#### exit 
  * go back to previous user
#### up and down arrow key
  * navigate the command you typed earlier
#### pwd
  * your location
#### ls 
  * what's in a current directory (list)
#### ls -l
  * long listing in vertical orientation
#### ls -a 
  * shows all the files (shows file starting with.)
#### ls -la or ls -l -a
  * shows all the files in the long listing command.
#### clear
  * clear the screen
#### ls -lh
  * (-h stands for human readable file sizes) (shows data in kilobytes and megabytes)
#### ls /bin
  * see what's in the bin directory (directly)
#### whoami 
  * gives the name of user or root.
#### Ctrl + C
  * requests that the program abort
#### man ls 
  * reference or help for commad ( hit arrow key to see more )
#### man man 
  * further reference ( hit arrow key to see more )
#### info
  * gives you information about various command lines ( you can hit arrow and navigate to the option with underlined text and press enter; press d to go back.
#### ls -a and less .bash_history 
  * shows all the command which are stored in bash history file from oldest to newest
#### command completion or autocomplete
  * type some words and press tab (you need not to type full word)
#### mkdir
  * make a directory
#### awk
    let's do create file by vim test.txt
    Type Your Name 
         Testing 1
         Hello World 
         Test 
         Just as Example
      save the file by (esc; shift-colon) wq
      1. awk '{print}' test.txt ---will print all
      2. awk '{print $1}' test.txt --will print 1st column
      3. awk '{print $2}' test.txt --will print 2nd column 
      4. awk '{print $1,$2}' test.txt --will print both 1st and 2nd column with space
      5. awk '{print $1.$2}' test.txt --will print both 1st and 2nd column without space
       
