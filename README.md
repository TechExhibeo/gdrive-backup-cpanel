# cpanel-backups-upload-to-gdrive
Automate Uploading of cPanel Created Backups to Google Drive using rclone

1) Clone this repo in /root directory of the server with directory name gdrive-backup-cpanel using following Command
 
 > git clone https://github.com/xaksh/gdrive-backup-cpanel -b cpanel+gdrive gdrive-backup-cpanel
 
 or you can use wget to download Zip Archive and Extract.
 
 > wget 'https://github.com/xaksh/gdrive-backup-cpanel/archive/cpanel+gdrive.zip'
 
 > unzip -j cpanel+gdrive.zip -d gdrive-backup-cpanel

2) Run setup.sh with Server Hostname, Host Node, Cron Job Time as arguments

 > source setup.sh "server.hostname.com" "swift" "30 5 * * *"

   server.hostname.com = Server's Hostname where Backup Script will run
   
   swift = Host Node name
   
   30 5 * * * = Backup Upload Script will run daily @5:30 AM

   Example: 
 > source setup.sh "swift.basezap.com" "swift" "30 5 * * *"
