

## 1. 行数

```shell
wc - l < filename
```

 常见选项：

-c 统计字节数 

-l 统计行数

-w 统计字数 

## 2. 查看文件内容



```shell
head -n filename # head -5 test.txt 查看test.txt前5行
sed -n ‘start,endp’ filname # stream editor
														# head -n '5,9p' test.txt 查看5-9行 
														# sed -n '5p' nowcoder.txt 
														# p 表示 print 打印
														# sed -n '/^\s*$/=' nowcoder.txt
														# ‘/../=’ sed 的正则模式  ^\s*$ 为正则表达式

tail -n filename # tail -5 test.txt 查看test.txt后5行
```

## 3.区间问题

```shell
{5..500..7} # 5 ~ 500区间 步长为7
```

## 4. 正则匹配

正则例子

- 邮箱

  - ```shell
    '^[a-zA-Z0-9._%+-]+@[a-ZA-Z0-9.-]+\.[a-zA-Z]{2,}$'
    ```

- 日期

  - ```shell
    '^\d{4}-\d{2}-\d{2}$'
    ```

- 手机号

  - ```shell
    '^1\d{12}$'
    ```

- 域名

  - ```shell
    'https?://([^/]+)'
    ```

- 浮点数

  - ```shell
    '^-?\d+(\.\d+)?$'
    ```

- IP地址

  - ```shell
    '(^25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.(^25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.(^25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.(^25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)$'
    ```

    

|         特殊字符和语法          |                             描述                             |                           例子                           |
| :-----------------------------: | :----------------------------------------------------------: | :------------------------------------------------------: |
|            普通字符             |                除特殊字符外，按字面意义匹配。                |                                                          |
|            点号 `.`             |                匹配任意单个字符，除换行符外。                |     正则表达式 `a.b` 可以匹配 "aab"、"a1b"、"a#b" 等     |
|         字符集 `[...]`          |                 匹配方括号内的任意一个字符。                 |      正则表达式 `[aeiou]` 匹配任意一个小写元音字母       |
|       反义字符集 `[^...]`       |               匹配不在方括号内的任意一个字符。               |        正则表达式 `[^0-9]` 匹配任意一个非数字字符        |
|          预定义字符集           | `\d` 匹配数字字符<br>`\w` 匹配单词字符<br>`\s` 匹配空白字符  |                                                          |
| 重复符号 `{n}`、`{n,}`、`{n,m}` |                   指定前面元素出现的次数。                   | `a{3}`：匹配连续三个 "a"<br>`a{2,4}`：匹配连续2到4个 "a" |
|     特殊字符 `*`、`+`、`?`      | `*` 匹配前面元素零次或多次<br>`+` 匹配一次或多次<br>`?` 匹配零次或一次 |                                                          |
|         分组 `( ... )`          |            将表达式分组，允许应用重复和其他操作。            |               `(abc)+` 匹配连续多个 "abc"                |
|          转义字符 `\`           |                      用于转义特殊字符。                      |                     `\\` 匹配反斜线                      |
|          锚点 `^`、`$`          |                 `^` 匹配开头，`$` 匹配结尾。                 |                                                          |
|         逻辑运算符 `|`          |                在多个模式中选择匹配其中之一。                |                  `a|b` 匹配 "a" 或 "b"                   |

## 5. 管道符 ｜

​		管道符是 Linux 系统中的一个特殊字符，用于将一个命令的输出作为另一个命令的输入。它通常用 `|` 表示，在命令行中输入 `|` 后再加上另一个命令即可实现管道操作 。

​		举个例子，如果你想查看当前目录下的所有文件，可以使用 `ls -l` 命令，然后使用管道符 `|` 将结果传递给 `less` 命令，以便一页一页地查看文件内容。具体命令如下：

```
ls -l | less
```

​		查找某个目录下的所有 .txt 文件，可以使用如下命令：

```
ls -l | grep ".txt"
```

​		这个命令的意思是先使用 `ls -l` 命令列出当前目录下所有文件的详细信息，然后通过管道符 `|` 将结果传递给 `grep` 命令，过滤出所有以 `.txt` 结尾的文件名。

管道符 `|` 和重定向符号 `>`、`>>` 是在命令行环境中用于处理输入和输出的特殊符号，它们有不同的作用和用途。

- **管道符 `|`：**

  - 管道符 `|` 用于将一个命令的输出作为另一个命令的输入。这允许您将多个命令链接在一起，以便在一个命令的输出上执行另一个命令的操作。

  - 示例：
    ```bash
    command1 | command2
    ```

  - 在这个例子中，`command1` 的输出会成为 `command2` 的输入。这对于数据处理、过滤和传递等场景非常有用。

- **重定向符号 `>` 和 `>>`：**

   - `>` 用于将命令的输出重定向到文件，并且如果文件已存在，则会覆盖该文件的内容。
   - `>>` 用于将命令的输出附加到文件末尾，而不会覆盖文件原有内容。
   - 示例：
     ```bash
     command > file.txt   # 将命令的输出覆盖写入到 file.txt
     command >> file.txt  # 将命令的输出追加写入到 file.txt
     ```
   - 这对于将命令输出保存到文件中或将输出添加到日志文件中非常有用。

- 区别：
  - 管道符 `|` 是将一个命令的输出传递给另一个命令的输入，通常用于将多个命令组合在一起以实现更复杂的操作。它不涉及文件的创建或修改。

  - 重定向符号 `>` 和 `>>` 则用于将命令的输出保存到文件中，可以用来创建、覆盖或追加文件内容。


- 举例来说，假设有一个命令 `command1`，它会在终端输出一些文本，您可以使用以下方式来处理其输出：
  - 使用 `command1` 本身，直接在终端显示输出。

  - 使用 `command1 > output.txt`，将输出保存到名为 `output.txt` 的文件中，并覆盖现有内容。

  - 使用 `command1 >> log.txt`，将输出追加到名为 `log.txt` 的日志文件末尾。


​        相比之下，如果要在 `command1` 的输出基础上执行另一个命令 `command2`，则可以使用管道符 `|`，如 `command1 | command2`。这将把 `command1` 的输出作为 `command2` 的输入进行处理。



## 6. 文本处理 grep awk sed



- **grep：**
   - `grep` 是 "Global Regular Expression Print" 的缩写，用于在文本中查找匹配某个模式的行，并将匹配到的行输出。
   - `grep` 基于正则表达式进行匹配，可以用来搜索包含特定模式的行。
   - 例子：`grep "pattern" file.txt` 将匹配文件中包含指定模式的行。

- **awk： ** NF 列数 NR 行数
   - `awk` 是一种处理文本数据的编程语言，也是一个命令行工具。它以行为单位处理文件，可以按列进行分割、提取、计算等操作。
   - `awk` 可以使用自定义的脚本来处理文本，对每一行应用脚本中定义的操作。
   - 例子：`awk '{ print $1 }' file.txt` 将提取文件中每一行的第一个字段并输出。

- **sed：**
   - `sed` 是 "Stream Editor" 的缩写，用于对输入流进行基本的文本转换和编辑操作。
   - `sed` 基于行进行操作，可以通过正则表达式来匹配和替换文本。
   - 例子：`sed 's/pattern/replacement/g' file.txt` 将替换文件中的特定模式为指定的字符串。

主要区别总结：
- `grep` 用于查找匹配行，是一个查找工具。
- `awk` 是一种强大的文本处理工具，可以进行更复杂的列处理和计算。
- `sed` 是一个基本的文本编辑工具，用于进行简单的替换和转换操作。

这些工具在实际应用中经常一起使用，通过管道将它们链接在一起，以便于处理复杂的文本处理任务。每个工具都有其特定的优势，根据需要选择合适的工具或组合来完成所需的任务。



- awk

  - `awk` 是一种用于文本处理和数据提取的强大命令行工具。它以行为单位处理文本文件，允许您在文本中查找模式、执行操作并输出结果。下面是一些常用的 `awk` 命令及其用法示例：

    - **基本语法：**

       ```bash
       awk 'pattern { action }' file
       ```

    - **打印整行：**
       ```bash
       awk '{ print }' file
       ```

    - **根据字段进行操作：**
       ```bash
       # 打印第一个字段
       awk '{ print $1 }' file
       
       # 打印前两个字段，以逗号分隔
       awk '{ print $1, $2 }' file
       ```

    - **使用分隔符：**
       ```bash
       # 使用冒号作为分隔符打印第一个字段
       awk -F':' '{ print $1 }' file
       ```

    - **使用条件：**
       ```bash
       # 打印包含关键词 "error" 的行
       awk '/error/ { print }' file
       
       # 打印第二列值大于 10 的行
       awk '$2 > 10 { print }' file
       ```

    - **计算和汇总：**

       ```bash
       # 计算第三列的总和
       awk '{ sum += $3 } END { print sum }' file
       ```

    - **自定义输出分隔符和结束动作：**

       ```bash
       # 使用冒号作为输出分隔符，并在结束时打印总行数
       awk -F':' '{ print $1, $2 } END { print "Total lines:", NR }' file
       ```

    - **更复杂的示例：**

       ```bash
       # 打印文件中每行的长度和内容
       awk '{ print "Length:", length, "Line:", $0 }' file
       
       # 打印文件中最长的行
       awk 'length > max_length { max_length = length; longest_line = $0 } END { print "Longest line:", longest_line }' file
       ```


  - ## awk语句

    - for循环

      - ```bash
        {for(i=1;i<+n;i++){if(length(si)<8){print $i}}}
        ```

        

    - 条件语句

      - ```bash
        BEGIN{sum=0}{sum+=$6}END{print sum}
        ```

    

- grep

  - ​		`grep` 命令是在Unix和类Unix系统中常用的文本搜索工具，用于在文件中查找匹配指定模式（正则表达式或普通字符串）的行。它的名称来源于 "Global Regular Expression Print"，意味着它的主要功能是查找匹配的行并将其打印输出。

    基本语法：

    ```bash
    grep [options] pattern [filename...]
    ```

    ​		其中，`options` 是一些可选的标志，`pattern` 是您要搜索的模式，`filename` 是要搜索的文件名。如果没有指定文件名，`grep` 将从标准输入读取数据。

    ​		常见的选项包括：

    - `-i`：忽略大小写。
    - `-v`：反向匹配，输出不包含匹配的行。
    - `-r`：递归搜索目录中的文件。
    - `-l`：只显示包含匹配的文件名，而不是匹配的行。
    - `-n`：显示匹配的行，并显示行号。
    - `-e pattern`：指定多个模式，可用于搜索多个字符串或正则表达式。
    - `-w`：仅匹配整个单词，而不是部分匹配。

    示例用法：

    - 在文件中搜索特定字符串：

       ```bash
       grep "apple" file.txt
       ```

    - 忽略大小写，搜索目录中所有文件：

       ```bash
       grep -i -r "banana" directory/
       ```

    - 输出不包含匹配的行：

       ```bash
       grep -v "cherry" file.txt
       ```

    - 仅显示包含匹配的文件名：

       ```bash
       grep -l "date" *.txt
       ```

    - 显示匹配的行和行号：

       ```bash
       grep -n "pattern" file.txt
       ```

    - 搜索多个模式：

       ```bash
       grep -e "apple" -e "banana" file.txt
       ```


- sed

  -  `sed` 命令的基本语法：

    ```
    sed [选项] '操作' 文件名
    ```

    ​	常用的选项有：

    - `-i`：直接修改文件内容（in-place）。例如：`sed -i 's/foo/bar/g' 文件名` 将文件中所有的 "foo" 替换为 "bar"。
    - `-e`：允许在一条 `sed` 命令中指定多个操作。例如：`sed -e 's/foo/bar/g' -e 's/baz/qux/g' 文件名`。
    - `-n`：取消自动打印模式空间的内容，只在显式要求的情况下打印。通常与 `p` 命令一起使用，例如：`sed -n 's/pattern/replacement/p' 文件名`。

      操作通常是由一个或多个 `sed` 命令构成的，每个命令由一个地址范围和一个动作组成，如下所示：


    ```
    [地址范围] 动作
    ```
    
    ​	常见的操作有：
    
    - `s/模式/替换内容/`：查找模式并将其替换为指定内容。例如：`sed 's/foo/bar/g' 文件名` 将文件中的 "foo" 替换为 "bar"。
    - `p`：打印模式空间中的内容。
    - `d`：删除模式空间中的内容。
    - `a\`：在当前行之后添加文本。
    - `i\`：在当前行之前插入文本。
    
    地址范围用于指定应用操作的行或行范围。例如：
    
    - `n`：仅在第 n 行应用操作。
    - `n,m`：在第 n 行到第 m 行之间应用操作。
    - `/模式/`：在匹配模式的行上应用操作。
    - `n~m`：从第 n 行开始，每隔 m 行应用操作。
    
    以下是一些 `sed` 的示例：
    
    - 替换文件中所有的 "apple" 为 "orange" 并输出结果：
       ```bash
       sed 's/apple/orange/g' 文件名
       ```
    
    - 删除文件中包含 "test" 的行：
       ```bash
       sed '/test/d' 文件名
       ```
    
    - 打印文件中包含 "error" 的行：
       ```bash
       sed -n '/error/p' 文件名b
       ```
    
    - 替换文件中第 10 行的 "old" 为 "new"：
       ```bash
       sed '10s/old/new/' 文件名
       ```


## 7. print 和 echo

- **语法：**

   - `print` 是一种在很多编程语言中用于输出文本的关键字，比如在像 AWK、Perl、Python 等脚本语言中使用。
   - `echo` 是一个常见的命令行命令，在大多数 Unix-like 操作系统上都可用，包括 Linux 和 macOS。

- **转义字符的处理：**
   - `print` 通常会自动处理转义字符，比如 `\n` 会被解释为换行。
   - `echo` 在某些系统中可能会不同，具体取决于使用的 shell。在大多数情况下，`echo` 会解释转义字符，但是在某些 shell 中，需要使用 `-e` 选项才能解释转义字符，如 `echo -e "Hello\nWorld"`。

- **选项和参数：**
   - `print` 在不同的编程语言和工具中具有不同的选项和参数。
   - `echo` 命令在命令行中是相对简单的，通常用法如下：
     ```bash
     echo "Hello, World!"
     ```

- **行为差异：**
   - 在某些情况下，`echo` 可能会处理一些特殊字符，如 `$`，导致变量展开。这可能会导致意外的行为，特别是在包含变量的文本中使用时。
   - `print` 在大多数情况下不会自动展开变量，通常会将字符串作为字面量输出。

## 9. 统计频率

- uniq -c

  - 

    ```bash
    uniq -c [输入文件]
    ```

    - `uniq`：此命令从已排序的文件中筛选出相邻的匹配行，并输出唯一的行。
    - `-c`：此选项告诉 `uniq` 在每行前加上连续出现在输入中的次数。如果没有连续的重复行，则计数为 1。
    - `[输入文件]`：这是可选参数，指定从中读取输入的文件。如果未提供，`uniq` 将从标准输入读取。



## 10. 排序

```bash
sort [选项] [输入文件]
```

常用的选项包括：

- 默认 按字典顺序

- `-r`：以逆序（降序）进行排序。
- `-n`：按照数值顺序进行排序，而不是字典顺序。
- `-u`：仅显示唯一的行，去除重复行。
- `-o 输出文件`：将排序结果保存到指定的输出文件中。
- `-k 列范围`：按照指定的列范围进行排序。

以下是一个示例：

假设你有一个名为 "numbers.txt" 的文件，内容如下：

```
5
20
10
3
```

运行命令 `sort -n numbers.txt` 将产生以下输出：

```
3
5
10
20
```



## 11. 参数传递

```bash
xargs [options] [command]
```

​		其中，`options` 是一些可选的标志，`command` 是您想要在参数上执行的命令。如果没有指定命令，`xargs` 默认会将参数传递给 `echo` 命令。

常见的选项包括：

- `-d delimiter`：指定分隔符，用于分割输入的数据。
- `-I replace-str`：指定一个占位符字符串，将其用实际的参数替代。
- `-n num`：指定每次传递的参数个数。
- `-P max-procs`：指定并行执行的最大进程数。
- `-t`：显示将要执行的命令，但不真正执行。

​		示例用法：

- 从文件中读取参数，并传递给 `echo` 命令：

   ```bash
   cat file.txt | xargs echo
   ```

- 删除一组文件：

   ```bash
   ls *.txt | xargs rm
   ```

- 使用 `-I` 替代字符串来执行命令：

   ```bash
   echo "file1.txt file2.txt" | xargs -I {} cp {} backup_{}
   ```

- 并行执行命令：

   ```bash
   cat list.txt | xargs -P 4 -n 1 wget
   ```

- 显示将要执行的命令：

   ```bash
   echo "file1.txt file2.txt" | xargs -t rm
   ```

​		请注意，`xargs` 默认以空白字符（空格、制表符、换行等）分隔参数。如果参数中包含特殊字符，可能需要使用 `-d` 选项来自定义分隔符。您可以通过运行 `man xargs` 命令在终端中查看完整的文档和选项列表。

## 12. 定时启动

​		在cron表达式中，星号 `*` 是一个通配符，表示“任意值”。它用于表示在相应的时间字段中可以匹配任何可能的值。

​		具体地说，在cron表达式中，星号 `*` 可以用于分钟、小时、日期、月份和星期的字段中，分别表示：

- **分钟字段（Minutes）：** `*` 表示匹配 0 到 59 之间的任意分钟数。
- **小时字段（Hours）：** `*` 表示匹配 0 到 23 之间的任意小时数。
- **日期字段（Day of Month）：** `*` 表示匹配 1 到 31 之间的任意日期。
- **月份字段（Month）：** `*` 表示匹配 1 到 12 之间的任意月份。
- **星期字段（Day of Week）：** `*` 表示匹配 0 到 6 之间的任意星期（0 表示星期日，1 表示星期一，以此类推）。

​		使用星号 `*` 可以使得相应的时间字段在每个可能的值上都触发定时任务。例如，如果您希望在每小时的每分钟都运行某个命令，可以在小时和分钟字段中都使用星号：

```
* * * * * /path/to/your/command
```

​		这将导致命令在每分钟都会被触发。

- 每天 23.55 执行

  - ```bash
    55 32 * * * 
    ```

- 每15分钟执行

  - ```bash
    15 * * * * 
    ```

## 练习

- **SHELL1** **统计文件的行数**

  - ```bash
    wc -l < nowcoder.txt
    ```

- **SHELL2** **打印文件的最后5行**

  - ```bash
    tail -5 nowcoder.txt
    ```

- **SHELL3** **输出 0 到 500 中 7 的倍数**

  - ```bash
    for n in {0..500..7}
    do
        echo $n
    done
    ```

- **SHELL4** **输出第5行的内容**

  - ```bash
    sed -n '5p' nowcoder.txt
    ```

- **SHELL5** **打印空行的行号**

  - ```bash
    grep -n '^\s*$' nowcoder.txt
    awk '/^\s*$/{print NR}' nowcoder.txt
    sed -n '/^\s*$/=' nowcoder.txt
    
    # grep使用: -n: 输出行号
    
    # //作为包含awk正则匹配模式的符号, NR属于awk内部变量,代表:已经读出的记录数,就是行号;
    
    # sed使用: -n：使用安静(silent)模式; //是sed正则表达式匹配模式, 最后一个=,＝作为sed命令打印行号: 例如(sed = nowcoder.txt),该命令会输出文件内容,且给每一行都加上行号,但是行号都在对应行内容的上一行,独立成行,因此使用-n,忽略内容等输出,只有经过sed特殊处理的那一行(或者动作)才会被列出来;
    ```

- **SHELL6** **去掉空行**

  - ```bash
    cat ./nowcoder.txt | awk NF
    ```

- **SHELL7** **打印字母数小于8的单词**

  - ```bash
    cat ./nowcoder.txt | awk -F" " '{for(i=1;i<=NF;i++){if(length($i) < 8){print $i}}}'
    ```

- **SHELL8** **统计所有进程占用内存百分比的和**

  - ```bash
    awk 'BEFIN{sum=0}{sum+=$4} END {print "所有进程占内存大小为：" sum}' nowcoder.txt
    ```

- **SHELL9** **统计每个单词出现的个数**

  - ```bash
    cat nowcoder.txt | xargs -n1 | sort | uniq -c | sort -n|awk '{print $2 $1}'
    ```

- **SHELL10** **第二列是否有重复**

  - ```bash
    cat nowcoder.txt | awk '{print $2}'| sort | uniq -c | grep -v '1' |sort -n
    ```

- **SHELL11** **转置文件的内容**

  - ```bash
    awk '{
        for(i=1;i<=NF;i++){
          if(NR==1){
            row[i] = $i;
          }else{
            row[i] = row[i]" "$i;
          }
        }
    }END{
      for(i=1;i<=NF;i++){
        print row[i]
      }
    }
    ' ./nowcoder.txt
    ```

- **SHELL12** **打印每一行出现的数字个数**

  - ```bash
    awk -F "[1-5]" 'BEGIN{sum=0}{print "line"NR" number:" (NF-1);sum+=(NF-1) }END{print "sum is" sum}' ./nowcoder.txt
    ```

- **SHELL13** **去掉所有包含this的句子**

  - ```bash
    grep -v 'this'
    ```

- **SHELL14** **求平均值**

  - ```bash
    awk '{if(NR==1) {N=$1} else{sum+=$1}} END{printf ("%.3f",sum/N) }'
    ```

- **SHELL15** **去掉不需要的单词**

  - ```bash
    grep -E -v "[bB]"
    ```

- **SHELL16** **判断输入的是否为IP地址**

  - ```bash
    # 使用正则表达式
    awk '{
         if ($0 ~ /^((25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.){3}(25[0-5]|2[0-4][0-9]|1[09][0-9]|[1-9][0-9]|[0-9])$/) {
             print("yes");
         } else if ($0 ~ /[[:digit:]].[[:digit:]].[[:digit:]].[[:digit:]]/){
             print("no");
         } else {
             print("error")
         }
     }' nowcoder.txt
    ```

- **SHELL17** **将字段逆序输出文件的每行**

  - ```bash
    awk -F ":" '{a[NR]=$NF; for (i=NF-1;i>0;i--) a[NR]=a[NR]":"$i }END{for(k in a) print a[k]}' nowcoder.txt
    ```

- **SHELL18** **域名进行计数排序处理**

  - ```bash
    awk -F "/" '{print $3}'| sort |uniq -c | sort -r| awk '{print $1" "$2}'
    ```

- **SHELL19** **打印等腰三角形**

  - ```bash
    #获取参数
    read n
    for ((i = 1; i <= n; i++)); do
    	#打印空格
    	for ((j = n - i; j >= 1; j--)); do
    		printf " "
    	done
    	#打印*
    	for ((k = 1; k <= i; k++)); do
    		printf "* "
    	done
    	#换行
    	printf "\n"
    done
    ```

- **SHELL20** **打印只有一个数字的行**

  - ```bash
    awk -F "[0-9]" '{if(NF==2){print $0}}' nowcoder.txt
    ```

- **SHELL21** **格式化输出**

  - 假设nowcoder.txt内容如下：

    > 1
    >
    > 12
    >
    > 123
    >
    > 1234
    >
    > 123456

    那么你的脚本输出如下：

    > 1
    >
    > 12
    >
    > 123
    >
    > 1,234
    >
    > 123,456

  - ```bash
    #!/bin/bash
    awk -F '' '{
        if(NF<=3){
            print $0
        } else {
            for(j=1;j<=NF;j++){
                if((NF-j)%3==0 && j!=NF){
                    printf("%d,",$j)
                } else {
                    printf($j)
                }
            }
            printf("\n")
        }
    }' nowcoder.txt
    
    ```

- **SHELL22** **处理文本**

  - 有一个文本文件nowcoder.txt，假设内容格式如下：

    > 111:13443
    >
    > 222:13211
    >
    > 111:13643
    >
    > 333:12341
    >
    > 222:12123

    现在需要编写一个shell脚本，按照以下的格式输出：

    > [111]
    >
    > 13443
    >
    > 13643
    >
    > [222]
    >
    > 13211
    >
    > 12123
    >
    > [333]
    >
    > 12341

  - ```bash
    awk -F ":" '{a[$1]=a[$1] $2 "\n"}END{for (i in a){printf("[%s]\n%s",i,a[i])}}' nowcoder.txt
    ```

- **SHELL23** **Nginx日志分析1-IP访问次数统计**

  - ```bash
    grep "23/Apr/2020" nowcoder.txt | awk '{print $1}'| sort | uniq -c | sort -r| awk '{print $1" "$2}'
    ```

- **SHELL24** **Nginx日志分析2-统计某个时间段的IP访问量**

  - ```bash
    grep "23/Apr/2020:2[0-3]" nowcoder.txt | awk '{print $1}'| sort -u |wc -l 
    ```

- **SHELL25** **nginx日志分析3-统计访问3次以上的IP**

  - ```bash
    awk '{print $1}' nowcoder.txt | sort | uniq -c | sort -r|awk '{if($1>3){print $1" "$2}}'
    ```

- **SHELL26** **Nginx日志分析4-查询某个IP的详细访问情况**

  - ```bash
    grep "192.168.1.22" nowcoder.txt | awk '{print $7}' | sort | uniq -c | awk '{print $1" "$2}'
    ```

- **SHELL27** **nginx日志分析5-统计爬虫抓取404的次数**

  - ```bash
    grep "baidu" nowcoder.txt | grep "404"| wc -l
    ```

- **SHELL28** **Nginx日志分析6-统计每分钟的请求数**

  - ```bash
    awk '{print $4}' nowcoder.txt| awk -F "/" '{print $3}' | cut -c '6-10'| sort  |uniq -c | sort -r | awk '{print $1" "$2}'
    ```

- **SHELL29** **netstat练习1-查看各个状态的连接数**

  - ```bash
    grep "tcp" nowcoder.txt | awk '{print $6}' | sort |uniq -c | awk '{print $2" "$1}' | sort -rn -k2
    ```

- **SHELL30** **netstat练习2-查看和3306端口建立的连接**

  - ```bash
    grep "3306" nowcoder.txt | awk '{print $5}' | awk -F ":" '{print $1}'| sort | uniq -c |sort -rn -k1 | awk '{print $1" "$2}'
    ```

- **SHELL31** **netstat练习3-输出每个IP的连接数**

  - ```bash
    awk -F ":" '/tcp/{print $2}'| awk '{print $2}' | sort | uniq -c | sort -rn | awk '{print $2" "$1}'
    ```

- **SHELL32** **netstat练习4-输出和3306端口建立连接总的各个状态的数目**

  - ```bash
    grep "3306" nowcoder.txt | awk '{print $5}'| awk -F ":" '{print $1}'|sort -u|wc -l | awk '{print "TOTAL_IP"" "$1}'
    grep "3306" nowcoder.txt | awk '{print $6}' | uniq -c | awk '{print $2 " "$1}'
    grep "3306" nowcoder.txt | wc -l | awk '{print "TOTAL_LINK"" "$1}'
    ```

- **SHELL33** **业务分析-提取值**

  - ```bash
    grep "Server version" nowcoder.txt | awk -F ":" '{print "serverVersion:"$4}'
    grep "Server number" nowcoder.txt | awk -F ":" '{print "serverName:"$4}'
    grep "OS Name" nowcoder.txt | awk -F ":" '{print $4}'| awk -F "," '{print "osName:"$1}'
    grep "OS Name" nowcoder.txt | awk -F ":" '{print "osVersion:" $5}'
    ```

- **SHELL34** **ps分析-统计VSZ,RSS各自总和**

  - ```bash
    awk '{sum_vsz+=$5;sum_rss+=$6}
    END{
        print("MEM TOTAL \n" "VSZ_SUM:" sum_vsz/1024 "M," "RSS_SUM:" sum_rss/1024 "M")}'
    ```

- **SHELL35** **删除第10行**

  - ```bash
    sed -i 10 filename
    awk 'NR!=10' filename > newfilename 
    
    ```

