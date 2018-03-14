# MongoDB的导入与导出

## MongoDB导入
### 导入CVS格式

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
mongoexport -h39.108.65.1 -ufxdt -pzhanGW -dood_cloud -cwm_shop_ -fsid,certificate --type=csv -o cert.csv

