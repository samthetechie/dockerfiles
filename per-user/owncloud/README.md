# Usage:

sudo docker build -t indiehosters/owncloud .
sudo docker run -d -e MYSQL_PASS=humptydumpty --name mysql indiehosters/mysql
sudo docker run -d -p 80:80 --link mysql:db -e DB_PASS=humptydumpty indiehosters/owncloud
curl -I http://localhost/