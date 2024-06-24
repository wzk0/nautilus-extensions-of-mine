## 自制 nautilus 好用的插件！

> 若你也有想法💡与新点子别忘了 `fork` 此仓库。

## 配置

nautilus 插件所在路径为：

```sh
/home/<用户名>/.local/share/nautilus/scripts
```

只需将所需插件下载 > 放在此文件夹并给予可执行权限即可。

### 0. 数列重命名

- 功能：将当前文件夹内所有文件重命名为数字排序的文件(1，2，3...)。

- 使用方法：右键当前文件夹任一文件执行即可(与右键哪个文件无关)。

- 源代码：

```python
#! /usr/bin/python3
import os
import sys

ls=os.listdir('.')
zero=1
for l in ls:
	f=l.split('.')[-1]
	os.system('mv "%s" "%s.%s"'%(l,zero,f))
	zero+=1
```
