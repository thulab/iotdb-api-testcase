# iotdb-api-testcase
iotdb-api-testcase

## 快速上手
### 1. 使用该`RESTful API`服务接口，需要在Iotdb的配置文件中，找到开关，开起服务。
```
# iotdb-datanode.properties
enable_rest_service=true
```
### 2.通过工具APIFOX编写API用例，然后导出APIFOX CLI格式文件

### 3. 环境部署及操作
当前为centos版本：
```
// Apifox CLI 依赖 Node.js 版本号 >= v16。使用前请先安装 Node.js.
dnf module install nodejs:18/common

//安装apifox-cli
npm install -g apifox-cli@latest

//通过以下命令确认是否安装成功
node -v && apifox -v && which node && which npm && which apifox
[root@i-flqv558n Apifox]# node -v && apifox -v && which node && which npm && which apifox
v18.9.1
1.2.41
/usr/bin/node
/usr/bin/npm
/usr/local/bin/apifox

//导出场景用例
//执行用例
apifox run testcase/user.apifox-cli.json -r cli,html
```
### 4.最后会生成一个HTML的测试报告
