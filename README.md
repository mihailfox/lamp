# Docker LAMP

1. Requirements:
    - Unix based machine or WSL
    - Docker engine and client (https://docs.docker.com/get-docker/)
    - Docker compose (https://docs.docker.com/compose/install/)
2. Ussage:
    - Clone the git repo to the desired dir (git clone <repo_address>)
    - Set executable bit to make_dirs.sh (chmod +x make_dirs.sh)
    - Run `./make_dirs.sh`
        - as a result the 3 default dirs will be created
            - html (mapped to /var/www/html/)
            - mysql-data (mapped to /var/lib/mysql)
            - httpd-etc (mapped to /etc/apache2, commented by default)
    - (optional) edit docker-compose.yml to adjust IP address and network
    - (optional) edit make_dir.sh and docker-compose.yml to change docker volumes
    - (optional) edit docker-compose.yml to add httpd
    - Run `sudo docker-compose up -d`
   
