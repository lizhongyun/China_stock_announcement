# China_stock_announcement
## 简介
* 该项目通过python脚本从巨潮网络的服务器获取中国股市（sz,sh）的公告(上市公司和监管机构),把公告信息放到数据库，公告文件下载到本地，并支持网页查询和读取。
* python用于公告下载和列表的数据库更新，node提供服务器的api调用和网页查询功能。

## 文件说明
* database：存放数据库的sql文件，以及监管机构的码表
* nodejs_query： 存放node服务的代码
* python_scraw:  存放python爬虫的程序
* 2plaintext：   存放一个python小脚本，用于将pdf、doc、docx文件转为纯文本文件。
## 使用
* 在python_scraw/cninfo_main.py中，修改合适的文件目录和日志目录以及数据库地址
* 按照database中的sql文件建立数据库
* 定期执行python cninfo_main.py sse(or regulator)
* 如需提供静态网站展示，可以用nodejs_query中的代码启动一个服务(注意相应的目录和sql查询语句与cninfo_main.py相对应)

