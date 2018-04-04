# MongoDB备份与还原

## MongoDB备份

mongodump -h hostname:port -d databaseName -o /backup/to/path/ -u userName -p password

## MongoDB还原
mongorestore -h hostname:port -d databaseName --dir /backup/to/path/ -u userName -p password

