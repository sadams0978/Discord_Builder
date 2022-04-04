# Discord_Builder
This will allow you to connect your Discord to a GitHub repo and build it.
I recommend creating a Systemd Service and telling it to run the Python script. This script will pull down your file from your GitHub Repo and then move it into the /var/www/html/ directory. Once it's moved there, it's on the Web Server. In my example, My GitHub repo is private so I will need to authenticate using an Token with GitHub. If yours is Public, then you will not need to authenticate and can just do a simple git clone. 


This script is made up of 2 files. 1 is the Python file that connects to Discord and whenever a message is sent it executes the script file. The script file actually authenticates against the GitHub repo and then moves the directory. It clears out whatever is in the Webserver before, so if you delete files, they will be deleted after the build. 
