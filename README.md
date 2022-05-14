# Docker LAMP

1. Requirements:
    - Unix based machine or WSL
    - Docker engine and client (https://docs.docker.com/get-docker/)
    - Docker compose (https://docs.docker.com/compose/install/)
2. Ussage:
    - Clone the git repo to the desired dir (git clone <repo_address>)
    - Set executable bit to make_dirs.sh
      - `chmod +x make_dirs.sh`
    - Run `./make_dirs.sh`
        - as a result the 3 default dirs will be created
            - html (mapped to /var/www/html/)
            - mysql-data (mapped to /var/lib/mysql)
            - httpd-etc (mapped to /etc/apache2, commented by default)
    - (optional) Edit `docker-compose.yml` to adjust IP address and network
    - (optional) Edit `docker-compose.yml` to change `mysql` passwords and database name
    - (optional) Edit `make_dir.sh` and `docker-compose.yml` to change docker volumes
    - (optional) Edit `docker-compose.yml` to uncomment `httpd-etc` and manualy configure `apache2`
    - Start LAMP using `sudo docker-compose up -d`
3. Transfer you website structure to `html` dir
4. Access your website via `http://<external_ip>:58080`
5. Access `mysql` via `<external_ip>:30306`
