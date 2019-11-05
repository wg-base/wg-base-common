# wg-base-common

##### Dcoker Container
- mysql
```
 image: mysql
 docker pull mysql:5.6.45
 docker run --name mysql -e MYSQL_ROOT_PASSWORD=root -d -p3307:3306 mysql:5.6.45

# 进入mysql
 docker exec -ti aabb bash
 mysql -uroot -p
 root

```
- redis
```
 image: redis
 docker pull redis
 docker run -d --name redis -p6379:6379 redis:latest --requirepass "root"
# 进入redis
 docker exec -ti aabb bash
 redis-cli
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
> use newdb 
# 删除数据库
> db.dropDatabase() 
# 创建collection 
> db.createCollection("user",{size:20,capped:true,autolndexld:true,max:50})
# 查询collection
> db.getCollectionNames()
> show collections
> db.getCollection("user")
> db.printCollectionStats()
# 删除collection
> db.user.drop()

文档级别操作
# 插入一条文档，我并没有创建集合student，直接写插入语句，如果表不存在会自动创建
> db.student.insert({"name":"xuye","school":"hafo","numbe":141420014}) 
# 再插入一条文档
> db.student.insert({"class":101,"number":1401420,"teach":"xuye"})
# 查看该集合中所有的文档。
> db.student.find()
# 格式化显示查询的语句
> db.student.find().pretty()
# 插入一条复杂一些的文档，可以嵌套，和json一样
> db.student.insert({"name":"xuye","number":140246,"deskmate":{"name":"xiaobai","number":140265}})
> db.student.insert({"name":"xuye","number":140246,"deskmate":[{"name":"xiaobai","number":140265},
{"name":"xiaohei","number":"142064"}]})

```
