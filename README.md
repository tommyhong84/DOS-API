# DOS-API


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

### tree -- 显示磁盘目录结构
---

```
usage: tree [盘符:][路径][/f][>prn]

1. /f 显示所在目录下面所有的文件，省略时，只显示目录，不显示文件
2. >prn 把所列目录及目录中的文件名打印输出. PS:demo的时候不成功

```

### deltree -- 删除整个目录
---

```
usage: deltree [盘符:][路径]

该命令可以一步将目录下面所有的文件、子文件、更下层的字幕里一并删除
小心使用. PS： 有的系统没有deletree.exe这个文件

1. deltree d:\dos-api\test

```

