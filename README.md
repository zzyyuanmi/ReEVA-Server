# 使用说明
这是一个正在施工中的项目，如果你要查看目前的效果请按照如下操作。

要运行与编译本项目，你需要最新版本的node与npm。

但是，我们推荐使用facebook出品的yarn而不是npm进行包的安装，yarn的安装请参阅[官方地址](https://yarnpkg.com/zh-Hans/docs/install)

接下来请在本目录下执行
```shell
yarn
```
这个操作将会安装项目依赖。

如果你不使用yarn，那末可以相应的执行
```shell
npm install
```

但是本命令有一定概率失败。

之后便可以通过
```shell
npm run gulp dev
npm run gulp build
npm run gulp test
```
分别开发（即watch模式）、编译、调试项目


目前上没有编写数据库的migration，如果你遇到问题，请删除`db/sqlite.db`

# 通过Docker开发
本项目目前包含了一个用于开发环境的Dockerfile, 仅内置了Node环境。可以尝试通过下列方式进入

```shell
docker build -t "zjueva/reeva:dev" .
docker-compose up -d
docker exec -it <your_container_name> bash
```