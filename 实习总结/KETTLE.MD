# :nut_and_bolt: Kettle
[返回总目录](../实习学习记录.md)
<!-- TOC -->

- [:nut_and_bolt: Kettle](#nut_and_bolt-kettle)
    - [组成](#%E7%BB%84%E6%88%90)
    - [文档](#%E6%96%87%E6%A1%A3)
    - [踩坑（暂时放弃源码部署，问题太多了，TODO）](#%E8%B8%A9%E5%9D%91%E6%9A%82%E6%97%B6%E6%94%BE%E5%BC%83%E6%BA%90%E7%A0%81%E9%83%A8%E7%BD%B2%E9%97%AE%E9%A2%98%E5%A4%AA%E5%A4%9A%E4%BA%86todo)
    - [lunux部署](#lunux%E9%83%A8%E7%BD%B2)
    - [一些简单教程](#%E4%B8%80%E4%BA%9B%E7%AE%80%E5%8D%95%E6%95%99%E7%A8%8B)

<!-- /TOC -->
## 1.组成
名称|描述
:-:|:-:
Spoon|通过图形接口，用于编辑作业和转换的桌面应用。
Pan|一个独立的命令行程序，用于执行由Spoon编辑的转换和作业。
Kitchen|一个独立的命令行程序，用于执行由Spoon编辑的作业。
Carte|Carte是一个轻量级的Web容器，用于建立专用、远程的ETL Server。

## 2. 文档
+ documents[--链接](https://wiki.pentaho.com/display/EAI/Latest+Pentaho+Data+Integration+%28aka+Kettle%29+Documentation)
+ Java API example[--链接](https://wiki.pentaho.com/display/EAI/Pentaho+Data+Integration+-+Java+API+Examples)
+ 源码[--链接](https://github.com/pentaho/pentaho-kettle/tree/9.0.0.0-R)
+ PDI系统[--链接](https://community.hitachivantara.com/s/article/data-integration-kettle)

## 3.踩坑（暂时放弃源码部署，问题太多了，TODO）
+ 源码部署踩坑：java jdk环境变量没配置,maven导入时报错No compiler is provided in this environment. Perhaps you are running on a JRE rather than JDK？注意是java jdk的环境变量，不是IDEA的
+ 部署的一些常见异常[--链接](https://www.e-learn.cn/topic/3193741)
+ EventManager这个类全局搜索时勾选“inclued non-project items"
+ 用8.x的版本重新试试[--链接1](https://blog.csdn.net/ifu25/article/details/103239489?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-2.nonecase&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-2.nonecase)[--链接2](https://blog.csdn.net/gongchengshiv/article/details/105211351)

## 4.lunux部署
+ 踩坑（包安装）
   + RedHat系列：redhat centos fedora,安装包格式rpm，包管理工具yum
   + Debian系列：Debian Ubuntu，安装包格式deb，命令dpkg，包管理工具apt-get
+ 图形界面问题路线：服务器上安装图形界面；本机利用Xmanager进行远程连接。（慢，太慢，能不能在本机写好ktr等文件后部署到服务器上？）
+ **服务器上定时执行kettle作业任务**（pan/kitchen/carte）[--参考](https://blog.csdn.net/zuolovefu/article/details/78083445)
+ **服务器上trans和job的执行** (job调用trans使用相对地址，具体要学一下怎么到上级目录,实现同级目录：${Internal.Entry.Current.Directory}/trans/test2.ktr）[--参考1](https://blog.csdn.net/harry5508/article/details/95377354)[--参考2](https://www.cnblogs.com/cc66/p/10254010.html)
+ **nohup相关**[--参考](https://blog.csdn.net/qq_29663071/article/details/81030396)
+ **carte**
   + 部署实践[--参考](https://www.jianshu.com/p/3cc0bc922c97)
   + 踩坑，端口bind问题[--参考](https://cloud.tencent.com/developer/article/1465705)

## 5.一些简单教程
+ **个人博客，涉及job，定时任务，优化等，不错**[--参考](https://blog.csdn.net/rotkang)

