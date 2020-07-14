#  :postbox: Mysql相关
[返回总目录](../实习学习记录.md)
## 1.连接mysql
+ 驱动用有drive.javad的，也就是5.x.x
+ mysql 8，常规链接有坑，配置data-integration\simple-jndi\jdbc.properties,后面加上
```
    heizhou/type=javax.sql.DataSource
    heizhou/driver=com.mysql.cj.jdbc.Driver
    heizhou/url=jdbc:mysql://localhost:3306/xxxx?useUnicode=true&characterEncoding=utf8&useSSL=false&serverTimezone=GMT // xxxx数据库名称
    heizhou/user=root 
    heizhou/password=xxxx  //密码
```
+ 选择方式jnbi。但是这样连接一次后JDBC方式就可以了，原因未知
+ 数据库编码问题 [--参考](https://www.cnblogs.com/cml-py/archive/2018/09/18/9668644.html)

## 2.基本操作
+ 简单抽取输出文本（txt）[--链接](https://blog.csdn.net/Auspicious_air/article/details/89850822)；文本读入数据库[--链接](https://blog.csdn.net/u013991521/article/details/52459431)
+ 同源数据库之间数据的抽取集成，读取后输出中插入更新，[--参考](https://blog.csdn.net/qqfo24/article/details/82190535)
+ oracle与mysql数据库之间数据迁移[--参考](https://blog.csdn.net/warrah/article/details/80197120)
+ 家里两台电脑数据库互连[--参考](https://blog.csdn.net/qq_36431281/article/details/88072719)