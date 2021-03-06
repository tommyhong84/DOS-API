# DOS-API

1. [cd -- 改变当前目录](https://github.com/Jackey-Sparrow/DOS-API#1-cd----改变当前目录)
2. [md -- 建立子目录](https://github.com/Jackey-Sparrow/DOS-API#2-md----建立子目录)
3. [rd -- 删除子目录](https://github.com/Jackey-Sparrow/DOS-API#3-rd----删除子目录)
4. [dir -- 显示磁盘目录](https://github.com/Jackey-Sparrow/DOS-API#4-dir----显示磁盘目录)
5. [tree -- 显示磁盘目录结构](https://github.com/Jackey-Sparrow/DOS-API#5-tree----显示磁盘目录结构)
6. [deltree -- 删除整个目录](https://github.com/Jackey-Sparrow/DOS-API#6-deltree----删除整个目录)
7. [del -- 删除文件](https://github.com/Jackey-Sparrow/DOS-API#7-del----删除文件)
8. [ren -- 文件改名](https://github.com/Jackey-Sparrow/DOS-API#8-ren----文件改名)
9. [copy -- 文件复制](https://github.com/Jackey-Sparrow/DOS-API#9-copy----文件复制)
10. [xcopy -- 目录复制](https://github.com/Jackey-Sparrow/DOS-API#10-xcopy----目录复制)



### 1 cd -- 改变当前目录
---

```
usage: cd [盘符:][路径][子目录名]

1. cd d:\\dos-api
2. cd.. 返回上一级
3. cd/  返回根目录

```


### 2 md -- 建立子目录
---

```
usage: md [盘符:][路径名]<子目录名>

1. md d:\dos-api\test 创建目录test
2. md d:\dos-api\test1\test 创建目录test1,并且在下面创建目录test

```

### 3 rd -- 删除子目录
---

```
usage: rm [盘符:][路径名][子目录名]
注意点：目录必须为空的才能删除，所以删除不是空的目录时候，需调用del命令删除下面所有的文件

1. del d:\dos-api\test1\*.* 删除test1目录下所有文件，不包括文件夹
2. rm d:\dos-api\test1 删除test1目录

```

### 4 dir -- 显示磁盘目录
---

```
usage: dir [盘符:][路径][/p][/w]

1. /p 当当前目录太多，无法再一屏显示，加上这个参数，可一次显示23行文件信息，提示任何键继续下一页
2. /w 只显示文件名，省略文件的大小和时间

```

### 5 tree -- 显示磁盘目录结构
---

```
usage: tree [盘符:][路径][/f][>prn]

1. /f 显示所在目录下面所有的文件，省略时，只显示目录，不显示文件
2. >prn 把所列目录及目录中的文件名打印输出. PS:demo的时候不成功

```

### 6 deltree -- 删除整个目录
---

```
usage: deltree [盘符:][路径]

该命令可以一步将目录下面所有的文件、子文件、更下层的字幕里一并删除
小心使用. PS： 有的系统没有deletree.exe这个文件

1. deltree d:\dos-api\test

```

### 7 del -- 删除文件
---

```
usage del [盘符:][路径][文件名] [\p]

1. /p  是否询问真要删除该文件
2. 不能删除属性为隐含或者只读的文件
3. 在文件名称中可以使用通配符
4. 删除所有文件可使用 del.

```

### 8 ren -- 文件改名
---

```
usage: ren [盘符:][路径][旧文件名] <新文件名>

1. ren d:\dos-api\test\aa.txt bb.js

```

### 9 copy -- 文件复制
---

```
usage copy [源盘:][路径]<文件名> [目标盘:][路径]<目标文件名>

1. 允许使用通配符 例如： *.* 实现多个复制
2. 复制时，目标文件名也可以与源文件名不相同，称作“异名拷贝”，此时，目标文件名不能省略
   copy d:\dos-api\test\aa.js d:\dos-api\test1\cc.js
3. 复制时，还可以将几个文件合并为一个文件，称为“合并拷贝”，格式如下：
		 copy d:\dos-api\test\aa.js+d:\dos-api\test\bb.js d:\dos-api\test1\dd.js

```

### 10 xcopy -- 目录复制
---

```
usage xcopy [源盘:][源路径] [目标源盘:][目标路径] [/s][/v][/e]

1. /s 对源盘下及子目录下面所有文件进行copy,除开指定/e参数。深度拷贝
2. /v 对拷贝的扇区进行校验

```

