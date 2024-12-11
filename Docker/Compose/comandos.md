# Compose

- sudo apt update
- sudo apt install -y docker.io
- sudo apt install -y docker-compose
- docker --version
- docker-compose --version
- mkdir mediawiki-docker
- cd mediawiki-docker
- nano docker-compose.yml
- docker-compose up -d
- docker-compose ps
- docker cp LocalSettings.php mediawiki:/var/www/html/

