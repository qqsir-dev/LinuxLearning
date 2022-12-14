### vim 命令总结

Vim 模式：分别是命令模式（Command mode），输入模式（Insert mode）和底线命令模式（Last line mode）

#### 光标移动命令

以下命令都是在命令模式下

1. 移动到行尾 $ 移动到行首 0
2. 移动到文章开头gg 移动到文章结尾 G（shift +g）
3. 跳到指定行:240 冒号+行号 或行号+G 12G
4. 向后移动一个单词 w 下一个单词尾部 e
5. 向前移动一句 ( 向后移动一句 )
6. 向前移动一段 { 向后移动一段 }
7. 向上翻一屏 ctrl+ f 向上翻一屏 ctrl+b

#### 启动vim命令

1. vim -r file 恢复上次异常退出的文件
2. vim + file 从文件的末尾开始 vim +num file 从文件的第num行开始
3. vim +/string file 将光标停留在搜索到的第一个string 位置

#### 插入命令

在输入模式下：

1. i 在光标前面插入
2. a 在光标后面插入
3. o 在下面新建一行插入
4. O 在上面新建一行插入
5. 退出插入模式 esc

#### 复制粘贴剪切

命令模式下

1. yy 或者Y 复制整行文本
2. y[n]w 复制1（n）个词
3. d[n]w 删除（剪切）1（n）个单词
4. [n]dd 删除（剪切） 1（n）行
5. p 粘贴到光标之后
6. P 粘贴到光标之前
7. D 删除剪切当前位置到末尾

#### 查找

在命令模式下：

1. /word 在文本中查找 word
2. n 向后查找下一个
3. N 向前查找下一个

#### 替换

在底线命令模式下

1. 😒/old/new 用new 替换当前行的第一个old
2. 😒/old/new/g 用new 替换当前行所有的old
3. :%s/old/new/g 替换所有的old

#### 排版

命令模式下

1. << 向左移动一个shiftwidth shiftwidth默认为4
2. 向右移动一个shiftwidth
3. [n] << 和[n]>> 光标一下的n行向左/向右缩进一个shiftwidth
4. 编辑代码文件可用= 进行代码自动缩进调整

#### 退出vim

在底线命令行

1. :wq 保存并退出
2. :q 退出当前窗口
3. :w 保存修改
4. :e! 重新加载当前文档并丢弃之前做的修改
5. :q!强制退出

#### Help

1. 在底线命令行 :help