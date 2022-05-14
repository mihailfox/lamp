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
            - httpd-etc (mapped to /etc/apache2, commented out by default)
    - (optional) Edit `docker-compose.yml` to adjust IP address and network
      - default docker internal network: `172.16.238.0/24`
      - Access `mysql` via
        - Address: `<external_ip or localhost>:30306`
        - communication between `php` and `mysql` is done on the internal network using `default port 3306` 
    - (optional) Edit `docker-compose.yml` to change `mysql` passwords and default database name
      -  Default credentials: 
         - `myuser:mypass123`
         - `root:root`
      - Default databse: `myapp`
    - (optional) Edit `docker-compose.yml` and `make_dir.sh`  to change docker volumes
    - (optional) Edit `docker-compose.yml` to uncomment `httpd-etc` and manualy configure `apache2`
3. Start LAMP using `sudo docker-compose up -d`
4. Transfer you website structure to `html` dir
5. Access your website via `http://<external_ip  or localhost>:58080`
