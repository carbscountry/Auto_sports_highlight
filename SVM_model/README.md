# Auto_sports_highlight_SVM 

## 起動方法


#### 0. 上の階層の docker-compose より、database コンテナを立ち上げる


#### 1. 下記コマンドでビルドとコンテナ起動を行う
```
$ docker-compose up -d app
```

#### 2. コンテナにアクセスし、ライブラリをインストール
```
$ docker-compose exec -it app /bin/bash

root@aa1519d1a400:/workspace# poetry lock
root@aa1519d1a400:/workspace# poetry install
```

#### 3. jupyter を起動
```
root@aa1519d1a400:/workspace# nbdime extensions --enable
root@aa1519d1a400:/workspace# chmod +x /workspace/code/DL_youtube/DL_fifa.sh
root@aa1519d1a400:/workspace# /workspace/code/DL_youtube/DL_fifa.sh
root@aa1519d1a400:/workspace# jupyter lab --allow-root --no-browser --NotebookApp.token='' --port 8888 --ip=0.0.0.0
```

#### 4. jupyter を開く
[http://localhost:8080/](http://localhost:8080/)