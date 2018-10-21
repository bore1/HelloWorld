awk、sed、grep更适合的方向：
https://www.w3cschool.cn/awk/c2li1k8d.html

 grep 更适合单纯的查找或匹配文本
 sed 更适合编辑匹配到的文本
 awk 更适合格式化文本，对文本进行较复杂格式处理
关于awk内建变量个人见解，简单易懂

解释一下变量：

变量：分为内置变量和自定义变量;输入分隔符FS和输出分隔符OFS都属于内置变量。

内置变量就是awk预定义好的、内置在awk内部的变量，而自定义变量就是用户定义的变量。

 FS(Field Separator)：输入字段分隔符， 默认为空白字符
 OFS(Out of Field Separator)：输出字段分隔符， 默认为空白字符
 RS(Record Separator)：输入记录分隔符(输入换行符)， 指定输入时的换行符
 ORS(Output Record Separate)：输出记录分隔符（输出换行符），输出时用指定符号代替换行符
 NF(Number for Field)：当前行的字段的个数(即当前行被分割成了几列)
 NR(Number of Record)：行号，当前处理的文本行的行号。
 FNR：各文件分别计数的行号
 ARGC：命令行参数的个数
 ARGV：数组，保存的是命令行所给定的各参数
自定义变量的方法

 方法一：-v varname=value ，变量名区分字符大小写。
 方法二：在program中直接定义。

 sort |uniq -c |sort -rn |head -n20
