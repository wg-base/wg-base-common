# wg-base-common

##### Dcoker Container
- [X] mysql
```
 image: mysql
 docker pull mysql:5.6.45
 docker run --name mysql -e MYSQL_ROOT_PASSWORD=root -d -p3307:3306 mysql:5.6.45

# 进入mysql
 docker exec -ti aabb bash
 mysql -uroot -p
 root

```
- [X]redis
```
 image: redis
 docker pull redis
 docker run -d --name redis -p6379:6379 redis:latest --requirepass "root"
# 进入redis
 docker exec -ti aabb bash
 redis-cli
```
- [X]mongo
```
 image: mongo
 docker pull mongo
 docker run -d -p27017:27017 --name mongodb mongo:latest


1.docker exec -ti e5ff bash
2.进入mongo  
控制台直接 mongo
3.mongo操作 
> db 
> use newdb 
> db.dropDatabase() 
> db.createCollection("user",{size:20,capped:true,autolndexld:true,max:50})
> db.getCollectionNames()
> show collections
> db.getCollection("user")
> db.printCollectionStats()
> db.user.drop()

文档级别操作
> db.student.insert({"name":"xuye","school":"hafo","numbe":141420014}) 
> db.student.insert({"class":101,"number":1401420,"teach":"xuye"})
> db.student.find()
> db.student.find().pretty()
> db.student.insert({"name":"xuye","number":140246,"deskmate":{"name":"xiaobai","number":140265}})
> db.student.insert({"name":"xuye","number":140246,"deskmate":[{"name":"xiaobai","number":140265},
{"name":"xiaohei","number":"142064"}]})

```
