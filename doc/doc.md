# 博客项目

## 项目需求
- 有超级管理员，可管理所有的用户，所有的文章等，所有的数据
- 用户可注册，登陆，编辑用户信息，管理文章



## 架构设计
- 采用微服务架构
- 使用go-micro，docker，
- mongo
- redis


## 进程设计

### SRV

- *user* 负责对用户表的管理
- *post* 负责对文章表的管理

### WEB
- *blog* 负责前端博客文章展示，后端渲染
- *dashboard* 负责普通用户进行博客文章管理，前端渲染, vue
- *super* 管理员页面，前端渲染, vue

### API
- *post* 文章管理, echo
- *user* 用户管理, echo

### proxy
- API
- WEB


### DB
- *mongo*

### cache
- *redis* 存储session，存储用户增长id



## 数据库表设计

- user

```json

{

    "_id": ObjectId,
    "id": "",
    "username":"",
    "password":"",
    "create_time":"",
    "modify_time":"",
    "permission":"",
}

```

- post
```json

{

    "_id": ObjectId,
    "id": "",
    "title": "",
    "content":"",
    "userId":"",
}

```


- permissions

```json
{
  "_id":ObjectId,
  "id": "",
  "name": "",
}

```






