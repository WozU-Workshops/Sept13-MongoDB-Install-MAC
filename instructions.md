#How to Install MongoDB on MAC

Go to MongoDB site and find the download button
Download tgz file a 64bit MAC operating system
Open your terminal and change directories to the downloads folder
cd downloads
ls 
Look at contents to show downloaded file
Unzip tgz
tar xzf nameOfFile.tgz
Moving unzipped file to mongodb folder in the local folder
sudo mv mongoblablahblah.tgz /usr/local/mongodb
We are now in the downloads for so we can run ls to see that it has been moved
Change directories to mongodb folder
cd /usr/local/mongodb
Need to create data/db folder
sudo mkdir -p /data/db
Manually change permissions of this folder (db)
sudo chown WHOAMI /data/db
Add All parts of mongodb to bash profile
Go back to home directory
cd
Open bash profile
Show all hidden files
ls-al (shows all hidden files)
Show bash profile
If file does not exist - create it
open .bash_profile
Now going to add export paths
export MONGO_PATH=/usr/local/mongodb
export PATH=$PATH:$MONGO_PATH/bin
Save file
Reload file in terminal
source .bash_profile
Check to see if Mongo is installed
Open 2 new terminals
Run the Mongo Demon by running mongod in one terminal
Run the Mongo client by running mongo in the other terminal
In the client terminal type show dbs to see databases 
Mongod in open terminal
Mongo in another client
show dbs
