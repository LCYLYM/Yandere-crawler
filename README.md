# Yande.re图片爬虫

## 前言

手动刷图费时费力，至少我是这么想的。于是就有了这个项目~~及后续更新~~。

本项目基于`Win7, Python3.5.2`与`Win10, Python3.6.7`开发，在`Ubuntu16.04, Python3.5.2`运行成功，其他环境未考虑。

## 功能

- 支持从指定的**开始页码**爬取到**结束页码**
- 也支持从**第一页**爬取到**上一次开始爬取的位置**
- 支持设置爬取的**图片类型**（全部、横图、竖图、正方形）
- 支持最大或最小**图片尺寸**、**宽高比**限制
- 支持限制爬取的**图片体积**
- 按照当天的日期创建目录并存放爬取的图片
- 爬取结束后会在图片目录下生成日志文件
- 支持**tag搜索与排除**
- (可选)**GUI**

## 如何使用

**可选**

编辑`config.json`中`folder_path`参数，设为自己想要的目录，如文件夹不存在将会自动创建。路径必须以斜杠结尾。

可接受的分隔符只有`/`或`\\`，`\`将被认为是转义字符而报错。

剩下的参数可以运行后根据提示修改。

Windows下命令行执行`python index.py`或`python GUI.py`均可，Linux下可直接执行。

## 注意事项

每次运行后`config.json`中`last_stop_id`参数会被自动修改为爬取到的第一张图片的ID，便于下一次爬取时只爬取新post，无论停止条件为ID或是页码。

## 更新日志

### 2.0

新增：tag搜索，图形界面~~与并行下载~~

### 1.0

终于完成了啦
