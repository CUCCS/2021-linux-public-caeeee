# shell脚本编程基础
## 一、实验环境
+ Windows 10
+ VirtualBox
+ Ubuntu 20.04 Server 64bit
+ VScode remote
+ imagemagick
## 二、实验报告要求
- 继承第一章：Linu基础（实验）的所有实验报告要求
- 任务的所有源代码文件必须单独提交并提供详细的** -help **脚本内置帮助信息（任务二、三的所有统计数据结果要求写入独立实验报告）
## 三、任务完成情况目录
- 任务一：用bash编写一个图片批处理脚本，实现以下功能：
    - [x] 支持命令行参数方式使用不同功能
    - [x] 支持对指定目录下所有支持格式的图片文件进行批处理
    - [x] 支持以下常见图片批处理功能的单独使用或组合使用 
      - [x] 支持对jpeg格式图片进行图片质量压缩
      - [x] 支持对jpeg/png/svg格式图片在保持原始宽高比的前提下压缩分辨率
      - [x] 支持对图片批量添加自定义文本水印
      - [x] 支持批量重命名（统一添加文件名前缀或后缀，不影响原始文件扩展名）
      - [x] 支持将png/svg图片统一转换为jpg格式图片
- 任务二：用bash编写一个文本批处理脚本，对以下附件分别进行批量处理完成相应的数据统计任务：
    - [x] 2014世界杯运动员数据 
        - [x] 统计不同年龄区间范围（20岁以下、[20-30]、30岁以上）的球员数量、百分比
        - [x] 统计不同场上位置的球员数量、百分比
        - [x] 名字最长的球员是谁？名字最短的球员是谁？
        - [x] 年龄最大的球员是谁？年龄最小的球员是谁？
- 任务三：用bash编写一个文本批处理脚本，对以下附件分别进行批量处理完成相应的数据统计任务：
    - [x] Web服务器访问日志 
        - [x] 统计访问来源主机TOP 100和分别对应出现的总次数
        - [x] 统计访问来源主机TOP 100 IP和分别对应出现的总次数
        - [x] 统计最频繁被访问的URL TOP 100
        - [x] 统计不同响应状态码的出现次数和对应百分比
        - [x] 分别统计不同4XX状态码对应的TOP 10 URL和对应出现的总次数
        - [x] 给定URL输出TOP 100访问来源主机
## 三、实验过程
### 环境准备
```
sudo apt-get update 
```
```
sudo apt-get install shellcheck
```
```
sudo apt-get install imagemagick
```
```
sudo apt-get install p7zip-full
```
```
wget "https://c4pr1c3.github.io/LinuxSysAdmin/exp/chap0x04/worldcupplayerinfo.tsv"
```
```
wget "https://c4pr1c3.github.io/LinuxSysAdmin/exp/chap0x04/web_log.tsv.7z"
```
### 任务一

- ```
  bash task1.sh -q
  ```
  [1-q](\image\1-q.png)
- ```
  bash task1.sh -r
  ```
  [1-r](\image\i-r.png)
- ```
  bash task1.sh -s
  ```
  [1-s](\image\i-s.png)
- ```
  bash task1.sh -p
  ```
  [1-p](\image\i-p.png)
- ```
  bash task1.sh -w
  ```
  [1-w](\image\i-w.png)
- ```
  bash task1.sh -t
  ```
  [1-t](\image\i-t.png)
- ```
  bash task1.sh -h
  ```
  [1-h](\image\i-h.png)
### 任务二
- [任务二结果](task2.md)
- ```
  bash task2.sh -a
  ```
  [2-a](\image\2-a.png)
- ```
  bash task2.sh -h
  ```
  [2-h](\image\2-h.png)
- ```
  bash task2.sh -n
  ```
  [2-n](\image\2-n.png)
- ```
  bash task2.sh -p
  ```
  [2-p](\image\2-p.png)
- ```
  bash task2.sh -s
  ```
  [2-s](\image\2-s.png)
### 任务三
- [任务三结果](task3.md)
- ```
  bash task3.sh -c
  ```
  [3-c](\image\3-c.png)
- ```
  bash task3.sh -f
  ```
  [3-f](\image\3-f.png)
- ```
  bash task3.sh -i
  ```
  [3-i](\image\3-i.png)
- ```
  bash task3.sh -o
  ```
  [3-o](\image\3-o.png)
- ```
  bash task3.sh -s
  ```
  [3-s](\image\3-s.png)
- ```
  bash task3.sh -u
  ```
  [3-u](\image\3-u.png)

## 四、参考资料
- [GIT-USR-BIN](https://www.bilibili.com/video/BV1jf4y1s7zd?p=2)
- [https://github.com/CUCCS/linux-2020-LyuLumos/blob/ch0x04/ch0x04](https://github.com/CUCCS/linux-2020-LyuLumos/blob/ch0x04/ch0x04)