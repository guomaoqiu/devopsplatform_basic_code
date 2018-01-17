简易的后台程序管理基础代码
登录、注册、邮件发送
更新提交 2018年01月17日15:00
可基于该基础代码作为模板，进行其他开发作业

##### 1.安装依赖包
```
pip install -r requirements.txt
```
##### 2.创建数据库时需要指定编码为UTF8;
```
CREATE DATABASE `DB_NAME` DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci;
grant all on DB_NAME.* to DB_USER@'127.0.0.1' identified by 'PASSWORD';
flush privileges;
```
##### 3.初始化数据库
```
python manager.py db init
python manager.py db migrate
python manager.py db upgrade
```
##### 4.初始化admin管理权限角色数据库
```
#python manage.py shell
from manager import Role
Role.insert_roles()
Role.query.all()
```
##### 5.Run
```
python manager runserver
```

