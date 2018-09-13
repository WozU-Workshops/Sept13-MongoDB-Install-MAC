# How to Install MongoDB on MAC


1. Go to MongoDB site and find the download button
2. Download tgz file a 64bit MAC operating system
3. Open your terminal and **change directories to the downloads folder**
   * First type in `cd downloads` to change directories
4. Look at contents to show downloaded file
    * Type `ls` in the terminal to show that the file has been downloaded
5. Unzip the .tgz file downloaded from the MongoDB site
    * Type `tar xzf <nameOfFile>.tgz` in the terminal to unzip the file
        * **Please note:** `<nameOfFile>` is replaced with the name of the actual file you downloaded off the MongoDB site.
6. Move the unzipped file from the downloads folder to the **mongodb** folder in the **local** folder
    * Type `sudo mv <nameOfFile>.tgz /usr/local/mongodb`
      * **Please note:** `<nameOfFile>` is replaced with the name of the actual file you downloaded off the MongoDB site.
7. Change directories from the downloads folder to /usr/local/mongodb
    * Type `cd /usr/local/mongodb` to change the directories
8. Now that we are in the mongodb directory, create a new directory */data/db*
    * Type `sudo mkdir -p /data/db `
9. Change the permissions of the directory just created
    * Type `sudo chown <whoami> /data/db` in the terminal
        * **Please note:** `<whoami>` needs to be replaced with your username for your computer. If you do not know it, you can type `whoami` in the terminal and it will return the username.
10. Add all necessary components to the the bash profile
    * Go back to the home directory
        * Type `cd` in the terminal to go back to the root
    * Show all hidden files in the root
        * Type `ls -al` in the terminal to show all hidden files
    * Scroll up to make sure you have the `.bash_profile` file listed
        * **Please note:**If you do not have the file, type `touch .bash_profile` to create it
    * Open bash profile
        * Type `open .bash_profile` in the terminal
    * The file will open in your default text editor. Add the following two lines to the end of the file:
        * `export MONGO_PATH=/usr/local/mongodb`
        * `export PATH=$PATH:$MONGO_PATH/bin`
    * Save the file
11. Reload the bash profile in the terminal
    * Type `source .bash_profile` to reload the bash profile
12. Check to see if Mongo is installed :)
    * Open **2** new terminal windows
        * In the first window, type `mongod` to start the Mongo Daemon
        * In the second window, type `mongo` to start the client
            * Remaining in the second window, type `show dbs` to show all the databases on the server. 
13. In a separate terminal window, you can open a 3rd window, type `mongo -version`. If you get a number, then you have successfully downloaded MongoDB!

