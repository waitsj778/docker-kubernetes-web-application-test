# 概要
debug用のPod

# 開発環境の注意点(2/20時点)
```
MacOSかつM1(Apple Silicon)
Docker for Mac のPreview版を使用
```
上記の条件に全て当てはまる場合はdockerコマンド実行時に`--platform linux/amd64`オプションをつける必要がある。

参考記事：[Macbook Pro M1(Apple Silicon) で Dockerを動かす](https://qiita.com/ao41/items/5feb96cd01c312407a2b)

# build
```
$docker build --platform linux/amd64 -t debug .
```
# run
```
$docker run -it --platform linux/amd64 debug sh
```
