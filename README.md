# wg-base-common

##### Dcoker Container
- mysql
```
image: mysql
docker pull mysql:5.6.45
docker run --name mysql -e MYSQL_ROOT_PASSWORD=root -d -p3307:3306 mysql:5.6.45
```
- redis
```
image: redis
docker pull redis
docker run -d --name redis -p6379:6379 redis:latest --requirepass "root"
```
