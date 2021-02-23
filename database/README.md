# Secretの作成
```
$openssl rand -base64 1024 | tr -d '\r\n' | cut -c 1-1024 > keyfile
$kubectl create secret generic mongo-secret \
--from-literal=root_username=<ユーザー名> \
--from-literal=root_password=<パスワード> \
--from-file=./keyfile
```

# weblog-db-pod.ymlへmerge
下記の情報をweblog-db-pod.ymlに整形して追記する
```
$kubectl get secret/mongo-secret -o yaml
```
# Secretリソースをmergeした後、Clean-upする
```
$kubectl delete secret/mongo-secret
```