# 查看MongoDB数据库大小
## 查看MongoDB中数据库的大小
查看所有数据库的大小<br>
> show dbs <br>
admin  0.000GB<br>
local  0.000GB<br>

查看指定数据库的大小<br>
> use dbname<br>
db.stat()<br>
注意：默认单位是字节<br>

以M为单位查看<br>
> db.stat(1024*1024)<br>

## 查看MongoDB数据库中某个集合的大小
> db.collectionName.stats() <br>

或者<br>
db.collectionName.storageSize();
