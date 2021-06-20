# Linux命令行使用基础
## 一、实验环境
+ Windows 10
+ VirtualBox
+ Ubuntu 20.04 Server 64bit
+ asciinema
## 二、实验目的
1. 下载并配置好asiinema
2. 阅读vimtutor，按照说明进行操作，用asciinema录制操作过程
3. 完成自查清单
## 三、实验过程
### 1. asciinema的安装与使用
    
- 通过cmd-ssh连接虚拟机，根据[官方提供的安装方法](https://asciinema.org/docs/installation)依次在命令界面输入如下代码：
    ```
    $ sudo apt-add-repository ppa:zanchey/asciinema
    $ sudo apt-get update
    $ sudo apt-get install asciinema
   ```
- 运行以下命令，在asciinema关联终端与在线账户。
    ```
    $ asciinema auth
    ```
- asciinema基本操作
    ```
    $ asciinema rec
    ```
- 结束录制
    ```
    $ exit
    ```
### 2. 学习vimtutor并分小节上传操作录像。
[lesson1](lesson1.md)

[lesson2](lesson2.md)

[lesson3](lesson3.md)

[lesson4](lesson4.md)

[lesson5](lesson5.md)

[lesson6](lesson6.md)

[lesson7](lesson7.md)
# 四、自查清单
1. 你了解vim有哪几种工作模式

    - 命令模式 
    - 插入模式 
    - 底行模式

2. Normal模式下，从当前行开始，一次向下移动光标10行的操作方法？如何快速移动到文件开始行和结束行？如何快速跳转到文件中的第N行？

    - 一次向下移动光标10行：`10j`
    - 移动到文件开始行和结束行：gg，结束行：`G`
    - 快速跳转到文件中的第N行：`Ngg、NG`

3. Normal模式下，如何删除单个字符、单个单词、从当前光标位置一直删除到行尾、单行、当前行开始向下数N行？

    - 删除单个字符：`x`
    - 删除单个单词：`dw`
    - 删除到行尾：`d$`
    - 删除单行：`dd`
    - 删除下N行：`Ndd`

4. 如何在vim中快速插入N个空行？如何在vim中快速输入80个-？

    - 插入N个空行：`No ESC` （O为在上插入，o为在下插入）
    - 快速插入80个-：`80i- ESC`

5. 如何撤销最近一次编辑操作？如何重做最近一次被撤销的操作？

    - 撤销最近一次编辑操作：`u`
    - 重做最近一次被撤销的操作：`Ctrl+R`

6. vim中如何实现剪切粘贴单个字符？单个单词？单行？如何实现相似的复制粘贴操作呢？

    - 剪切单个字符：`x`
    - 剪切单个单词：`dw`
    - 剪切单行：`dd`
    - 复制单个字符：`y`
    - 复制单个单词：`b` `yw`
    - 复制单行：`yy`
    - 粘贴操作都是：`P` 
    - Visual模式下选择好范围, `d` 剪切，`y` 复制，`p` 粘贴

7. 为了编辑一段文本你能想到哪几种操作方式（按键序列）

    - 光标移动：`h`,`j`,`k`,`l`,`w`,`b`,`Ctrl+b`,`Ctrl+f`,`gg`,`G`
    - 编辑操作（插入或替换）：`i`,`a`,`o`,`cw`
    - 删除操作：`x`,`dd`,`dw`,`D`
    - 查询操作：/[search]
    - 退出：:`wq`,`:q`,`:q!`

8. 查看当前正在编辑的文件名的方法？查看当前光标所在行的行号的方法？
    - 查看文件名`:f`
    - 查看当前所在行号`Ctrl-g`

9. 在文件中进行关键词搜索你会哪些方法？如何设置忽略大小写的情况下进行匹配搜索？如何将匹配的搜索结果进行高亮显示？如何对匹配到的关键词进行批量替换？

    - 关键词搜索：`/pattern`
    - 设置忽略大小写：`:set ignorecase` `:set ic`
    - 高亮显示搜索结果：`:set hlsearch :set hls`
    - 关键词进行批量替换：:`%s/old/new/g`

10. 在文件中最近编辑过的位置来回快速跳转的方法？

    - `Ctrl-o`
    - `Ctrl-i`

11. 如何把光标定位到各种括号的匹配项？例如：找到(, [, or {对应匹配的),], or }

    - 光标移至需要匹配的括号上 `%`

12. 在不退出vim的情况下执行一个外部程序的方法？

    - `:!+外部命令`

13. 如何使用vim的内置帮助系统来查询一个内置默认快捷键的使用方法？如何在两个不同的分屏窗口中移动光标？

    - 查询一个内置默认快捷键 `:help [参数]`
    - 在两个不同的分屏窗口中移动光标`Ctrl+w+[h | j | k | l]`

## 五、参考资料
[vim学习笔记——vimtutor](https://www.jianshu.com/p/dbd02f28bc0c)