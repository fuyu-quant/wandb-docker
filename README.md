# wandb-docker
<img src="image/wandb.png" width="200">
wandb docker


## Contents
* [Basic docker operations](#basic-docker-operations)
* [wandb](#wandb)
* [Reference](#reference)



## [Basic docker operation](https://github.com/fuyu-quant/dockerfile-for-data-scientists)


## wandb

### wandbの起動
* コンテナ起動時に起動
初期設定では以下のdockerfileのコードによりコンテナ起動時に実行するようになってる
```bash
ENTRYPOINT ["wandb", "run", "src/app.py", "--server.port=8060", "--server.address=0.0.0.0"]
```

* コマンドで起動
```bash
# コンテナ外部から起動
docker-compose exec wandb bash "wandb run src/app.py --server.port=8060 --server.address=0.0.0.0"
```
When you want to exit, press [control + c]

* Link
http://127.0.0.1:9010/

## Reference
* https://github.com/wandb/server