# 文件和目录等操作

- ## 基本操作

    - cp--复制

    - mv--移动或者是重命名

    - mkdir--创建一个目录文件(通俗讲也就是说创建一个目录只不过Linux处处皆文件故称之)

    - rm--删除文件

    - ln--创建硬连接

- ## 通配符

    > 通配符其实也就代称相当于css中的选择器

    - 通配符的匹配关键符号：<br><br>![p](../picture/tong.png) 

    - 通配符的关键符号的一些具体用法：<br><br>![p](../picture/tong-1.png)

    - 一些经典案例：<br><br>![p](../picture/tong-e.png)
- ## mkdir

    - 基本用法：`mkdir file1 file2 file3...`可以同时创建多个文件

- ## cp

    - 基本用法：<br><br>![p](../picture/cp-opinios.png)

    - 用法案例：<br><br>![p](../picture/cp-example.png)

- ## mv

    - 移动或者是重命名文件

    - opinions:<br><br>![p](../picture/mv.png)

    - 用法案例：<br><br>![](../picture/mv-1.png)

- ## `rm`

    - rm含义是：删除文件或者目录

    - opinions<br><br>![](../picture/rm.png)

    - example:<br><br>![](../picture/rm-1.png)

    - `rm -f`意思是删除文件夹和文件夹中的文件，但是如果里面都是空的话，这个命令就无法使用。

- ## `rmdir`
    - 删除文件夹
    - opinions:
        - `-p`也就是删除输入路径的所有内容
        ```bash
        rmdir -p /s/ss
        ```

        - 这样的结果就是ss和s都没有了也就是当子目录被删除后如果父目录也变成**空目录**的话，就连带父目录一起删除。

    - 删除文件和文件内所有内容不妨可以这么做`rmdir ./example/* `然后在`rmdir ./example`这样就没问题了不存在文件夹是空的啊或者是文件夹不是空的啊文件夹不是文件啊这种错误了

- ## rm rmdir 总结：

    - rm删除文件和文件夹，但是使用的时候通常会显示出，这个文件是文件夹无法删除的字样。通常一个文件夹里只有一个文件的话使用`rm -r`可以删除文件和这个文件夹，如果不是只有一个文件的话，那么这个文件夹是不能被删除的。

    - rmdir删除的是文件夹，不能删除文件，如果想删除文件夹和文件夹中的所有文件可以使用`rmdir ./name/*`先删除所有的内容然后使用`rmdir ./name`就可以删除这个空的文件夹了。

- ## ln
    - 硬连接和软连接(也叫符号连接)的命令

    - `ln file link`硬连接file是文件后面是原路径
    
    - `ln -s item link`软连接