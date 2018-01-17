简易的后台程序管理基础代码
登录、注册、邮件发送
更新提交 2018年01月17日15:00

可基于该基础代码作为模板，进行其他开发作业


pip install -r requirements.txt

python manager runserver 

python manager.py db init

python manager.py db migrate

python manager.py db upgrade

    # 创建数据库时需要指定编码为UTF8;
        # CREATE DATABASE `xiangce` DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci;
        # grant all on local_ops.* to local_ops@'127.0.0.1' identified by 'local_ops';
        # flush privileges;
        #
        #python manage.py shell
        from manager import Role
        Role.insert_roles()
        Role.query.all()
