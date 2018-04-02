# MongoDB的增查改删
## MongoDB插入数据
## MongoDB查找数据
**获取某个集合所有的数据**<br>
db.getCollection('collectionName').find()<br>

**只获取某个集合中10条记录**<br>
db.getCollection('collectionName').find().limit(10)<br>

**按某个字段排序后获取前10条记录**<br>
db.getCollection('collectionName').find().sort({fieldName:-1}).limit(10)<br>
注：fieldName为排序的字段名，1为升序，-1为倒序<br>

## MongoDB修改数据<br>
## MongoDB删除数据<br>

**清空某个集合的所有记录** <br>
> db.collectionName.remove({}); # 这类似MySQL中的truncate命令。<br>
> db.collectionName.find({}).count() #  检查是否已成功删除<br>

**删除满足指定条件的记录** <br>
> db.collectionNam.remove({'collect_date':{$gt:new Date(2018,2)}})
