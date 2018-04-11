# MongoDB的导入与导出

## MongoDB导入
### 导入CVS格式
语法：mongoimport -h hostname -u username -p password -d dbName -c collectionName --headerline --type=csv --file fileName.csv<br>
参数说明：
* h: host简写，主机名
* u: user简写，用户名
* p: password简写，密码
* d: database简写，数据库名
* c: collection简写，多个之间用逗号间隔
* headerline: 加上它表示用csv首行作为字段名
* type：导入类型，可选值为csv和json
* file: 导入文件<br>
**使用示例**<br>
mongoimport -h 192.168.104.10 -u test -p testpwd -d networods -c product --headerline --type=csv --file ~/cache.csv<br>

## MongoDB导出
### 导出csv格式
语法：mongoexport -h hostname -u username -p password -d dbName -c collectionName -f field --type=csv -o cert.csv <br>
参数说明：
* h: host简写，主机名
* u: user简写，用户名
* p: password简写，密码
* d: database简写，数据库名
* c: collection简写，多个之间用逗号间隔
* f: field简写，字段，多个之间用逗号间隔
* type：导出类型，可选值为csv和json
* o: output简写，输出文件<br>
**使用示例：**
mongoexport -h 39.108.65.1 -ufxdt -pzhanGW -dood_cloud -cwm_shop_ -fsid,certificate --type=csv -o cert.csv

### 带有查询条件的导出
语法：在前面的基础上增加--query JSONString即可。示例如下：<br>
mongoexport -h39.108.65.1 -ufxdt -pzhanGW -dood_cloud -cwm_shop_ -fsid,certificate --query "{'md5_code': '00004492a07eb4240bedfe14f46d9af7'}" --type=csv -o cert.csv
