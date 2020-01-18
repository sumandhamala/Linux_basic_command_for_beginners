## Linux_basic_command_for_beginners
#### vim or vi
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
#### awk and grep
    let's do create file by vim test.txt
    Type Your Name 
         Testing 1
         Hello World 
         TesT
         123 Testing
      save the file by (esc; shift-colon) wq
      1. awk '{print}' test.txt ---will print all
      2. awk '{print $1}' test.txt --will print 1st column
      3. awk '{print $2}' test.txt --will print 2nd column 
      4. awk '{print $1,$2}' test.txt --will print both 1st and 2nd column with space
      5. awk '{print $1.$2}' test.txt --will print both 1st and 2nd column without space
      6. awk '/test/ {print}' test.txt --will print nothing as it is case sensative
      7. awk '/Test/ {print}' test.txt --will print Testing 1 and 123 Testing 
      8. awk '/TesT/ {print}' test.txt --will print TesT
      9. awk '/[a-z]/{print}' test.txt --will grab every line that contains at least one lower case letter
      10. awk '/[0-9]/{print}' test.txt --will grab every line that contains numbers
      11. awk '/^[0-9]/{print}' test.txt --will show every line that starts with a number
      12. awk '/[0-9]/${print}' test.txt --will show every line that ends with a number
      13. awk '{if($1~/123/) print}' test.txt --will print 1st column equals to 123 i.e. 123 Testing
      14. awk '{if($1~/[0-9]/) print}' test.txt --will print 1st column equals to number i.e. 123 Testing
      15. awk '{if($2~/[0-9]/) print}' test.txt --will print 2nd column that is equal to number i.e. 1 Testing
      
      GREP
      
      1. grep -i test test.txt --search for everything that has test
      2. grep -i test test.txt | awk '/^[0-9]/{print}' --will print 123 Testing 
      
      For ex: if you overwrite by 
         Testing 1: abdsfadf
         Hello World: how r you
         TesT:blabla
         123 Testing: what's going on
       1. awk -F: '{print $2}' test.txt --will return 2nd column after the colon
       2. awk -F: '{print $1}' test.txt --will return 1st column before the colon
       
       For ex: if you overwrite by
          "field1","field2","field3"
        1. awk -F "," '{print $3}' test.txt --will print "field3"
        2. awk -F "," '{print $3}' test.txt | sed 's/"//g' -- will print field3 by extracting string between doulbe quotes
        3. awk -F "," '{print $3}' test.txt | sed 's/"/rock/g' --will print rockfield3rock
        4. awk -F "," '{print $1,$3}' test.txt | sed 's/"/rock/g' --will print rockfield1rock rockfield3rock
   #### for loop
       for sth in {1..5}
       do
       echo $sth
       done --- will print 1 to 5
   #### to save file after grep and awk
        1. awk '{if($2~/1/)print}' mainfile.csv>>newfile.csv--will save second column with value 1 in new file
        2. grep -i 1 mainfile.csv>>newfile.csv --will save the file having value 1 in new file
        3. > means to save a file by complete overwrite.
        4. >> means to save a file by adding content at the end of the file or append a line
        5. echo "success" --which helps you to see if the script worked on real
        6. after vi script.sh and writing the above code run sh script.sh, you should see success
#### tee command
  * echo $(date) > abc.txt   is equal to == date | tee abc.txt
  * echo $(date) >> abc.txt is equal to == date | tee -a abc.txt
#### netstat command
  * netstat -anp || grep LISTEN   ---- will show all ports opened
#### telnet
  * telnet IP_add 8080  -- will show if you have 8080 port open in that IP. If it's opend it gives connected message
