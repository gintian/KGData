# KGData
 各个行业知识图谱分享，关系抽取，数据清洗，提供 neo4j 批量导入格式
 
 __Menu__

| Topic                                    | Description                              |
| :--------------------------------------- | :--------------------------------------- |
| <a href="#百科数据">百科通用数据</a> | 百科通用数据 |

# 《百科数据》

中文知识图谱，4000w实体，一亿关系，这是我精心整理、清洗、去重后的数据，数据格式已经处理，可用 neo4j-admin 直接导入，所有数据来源都是公开的百科或新闻数据。

以下给出了部分数据，并附上了使用步骤，适合研究生交作业用，接受定制服务

## 使用步骤

### 1.首先你要自行安装 neo4j

### 2.由于本方式是覆盖导入，建议创建一个全新的知识图谱库

### 3.解压后将两个文件放入 import 目录

### 4.执行导入语句
```
bin/neo4j-admin import --id-type=STRING --multiline-fields=true \
                       --nodes "import/entity10.csv"  \
                       --relationships "import/relationship10.csv" \
```

                       
导入成功显示如下：
```
IMPORT DONE in 3s 337ms. 
Imported:
  100000 nodes
  88362 relationships
  288361 properties
Peak memory usage: 1.03 GB
```

### 5.启动 neo4j，查看导入的数据

`MATCH (ee:my_entity) WHERE ee.name = "文天祥" RETURN ee;
`
点击展开子节点，返回效果如下
![image](https://github.com/chriswangweb/KGData/blob/master/img/1578500414912.jpg)



# 联系作者

#### 公众号：作者微信：,作者邮箱联系方式：chris.wang.web@gmail.com

捐赠作者（捐赠将用来购买服务器，OSS，更快的处理速度，更多的数据，更快的下载速度）
![image](https://github.com/chriswangweb/KGData/blob/master/img/IMG_1597.JPG)
![image](https://github.com/chriswangweb/KGData/blob/master/img/WechatIMG102.jpeg)