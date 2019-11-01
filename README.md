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
- mongo
```
image: mongo
docker pull mongo
docker run -d -p27017:27017 --name mongodb mongo:latest


1.docker exec -ti e5ff bash
2.进入mongo  
控制台直接 mongo
3.mongo操作
# 显示数据库 
> db 
# 切换数据库
# 删除数据库
# 创建collection 
# 查询collection
# 删除collection
  


```
