# 饭团小说
开源小说阅读app，切勿用于不当用途。造成一切后果与本人无关。

[下载应用](http://yourbuffslonnol.com)


## 小说源
两种方式获取小说内容，一种追书神器api，一种爬取盗版小说站。

### 追书神器api
在项目的api文件里有详尽的接口说明。来源于网络。

### 爬虫
重点说说爬虫的实现。考虑到旧版追书的api（新版的都用https）随时都可能会关闭。刚开始只是实现爬虫的，
本着学习的心态（人话：主要还是考虑到请求速度还有质量）。

## 对爬虫的要求：  
   ### 不升级app能修改爬虫。  
   ### 不升级app能增加盗版站的爬虫。
  
### 使用方案是，通过动态加载jar包反射里面的方法，获取小说内容，jar包又能通过服务器下载。o啦。


#### 制作爬虫步骤：  

  ##### 0.参考module包里面的 BooFactory_xxxxx类。
  
  ##### 1.继承 com.anonymouser.book.module.IBookLoadFactory  
  
  ##### 2.实现 getZhangjie 方法，实现爬取章节标题和章节的链接。
  
  ##### 3.实现 getBook 主体内容的爬虫。
  
  ##### 4.实现 getVersion 该爬虫的版本号，考虑到网站会改变。
  
  ##### 5.打包类为jar包，如何打包成jar包（略），打包后参考assets/jar，也可以放在服务器，实现更新爬虫，添加爬虫。
  
  
  
##成型
![][readme/0.png]  
![][readme/1.png]  
![][readme/2.png]  
![][readme/3.png]  
![][readme/4.png]







































