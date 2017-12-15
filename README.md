ofo共享单车地图爬虫
====================

```

感谢您的支持
朋友要做城市数据的一些研究，拜托我写ofo地图的小爬虫
最初的看到了derekhe大神写的单车地图，觉得非常的优秀。
但是单车地图由于封杀官方不断封杀爬虫的行为，被迫关闭了。
derekhe写的爬虫也没办法使用了，于是参考了derekhe的代码。
对现在ofo的api进行了分析，实现了对ofo附近单车位置的爬取。
```

该爬虫为ofo附近单车爬虫
* 目前只支持ofo
* 多线程爬取
* 自动去重
* 输出csv文件，存放在db/【日期】/【日期】-【时间】-【品牌】.csv文件内
* gzip压缩存储

# 运行环境
* Python3
* Linux/Mac/Windows

请根据你的需要修改配置文件config.ini，请查看内置说明。

## Linux/Mac
* 下载[最新代码](https://github.com/SilverBooker/ofoSpider/archive/master.zip)并解压
* 修改config.ini确保坐标和区域等参数正确
* 运行：
```
pip3 install -r requirements.txt
python3 run.py
```

## Windows
* 下载[最新代码](https://github.com/SilverBooker/ofoSpider/archive/master.zip)并解压
* 安装好python3.5.3
* 在cmd中执行pip install -r requirements.txt
* 修改config.ini确保坐标和区域等参数正确
* 在cmd执行python run.py

# 输出格式

输出格式：CSV

每行格式：时间戳，单车编号，经度，纬度
