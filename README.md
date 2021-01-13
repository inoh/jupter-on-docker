# Jupyter notebook on Docker

## 前提条件

- Docker がインストール済みであること
- git がインストール済みであること

## 動かし方

```shell
$ git clone https://github.com/inoh/jupter-on-docker.git
$ mkdir notebook
$ docker-compose run --rm jupyter python -c 'from notebook.auth import passwd;print(passwd())'
$ [password を入力]
$ docker-compose up # 起動時に token がコンソールに表示されるので確認しておく
```

`http://localhost:8888` にアクセスする  
表示される画面に token とパスワードを入力してログインする。  
