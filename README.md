    * Continuation of the Airbnb project
I was tasked to deploy the project onto given servers
The project is a continuation of Airbnb v1 and v2 where I paired with cohort mates, Leah Kagure and Ndege Monda respectively to complete both versions.
I have forked the repository from my previous partner, Ndege Monda to learn how to deploy the app to running servers using tools like Puppet, Fabric and by use of shell scripts.

### __ 0-setup_web_static.sh __ :
Sets up your web servers for the deployment of web_static.
The script:
    * Installs Nginx if it not already installed
    * Creates the folder /data
    * Creates the folder /data/web_static
    * Creates the folder /data/web_static/releases
    * Creates the folder /data/web_static/shared
    * Creates the folder /data/web_static/releases/test
    * Creates a fake HTML file /data/web_static/releases/test/index.html (with simple content, to test your Nginx  configuration)
    * Creates a symbolic link /data/web_static/current linked to the /data/web_static/releases/test/ folder. If the symbolic link already exists, it should be deleted and recreated every time the script is ran.
    * Gives ownership of the /data/ folder to the ubuntu user AND group.
    * Updates the Nginx configuration to serve the content of /data/web_static/current/ to hbnb_static (ex: https://mydomainname.tech/hbnb_static). Don’t forget to restart Nginx after updating the configuration:
    * Uses alias inside your Nginx configuration