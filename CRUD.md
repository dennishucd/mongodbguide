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
**修改某个集合中的某个字段的值** <br>
db.collectionName.update({'md5_code':'5eb594d6cacca705fac976e96704d1b1'}, {$set:{'status':NumberInt(0)}})<br>
注意：mongodb将数字默认为double类型，由于本例中的status为Int32，因此需要加转换，否则字段类型会被改变。<br>

## MongoDB删除数据<br>

**清空某个集合的所有记录** <br>
> db.collectionName.remove({}); # 这类似MySQL中的truncate命令。<br>
> db.collectionName.find({}).count() #  检查是否已成功删除<br>

**删除满足指定条件的记录** <br>
> db.collectionNam.remove({'collect_date':{$gt:new Date(2018,2)}})
