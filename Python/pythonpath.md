# PYTHONPATH

在执行python脚本的时候经常会遇到找不到包的情况


如：在/User/frankie目录下写了一个脚本foo.py。但是在python解释器中直接import是会报错的。


```shell

In [3]: import foo
---------------------------------------------------------------------------
ModuleNotFoundError                       Traceback (most recent call last)
<ipython-input-3-7f58dd7fb72e> in <module>
----> 1 import foo

ModuleNotFoundError: No module named 'foo'

In [5]: import sys

In [6]: sys.path
Out[6]:
['/Users/frankie/.pyenv/versions/3.6.5/bin',
 '/Users/frankie/.pyenv/versions/3.6.5/lib/python36.zip',
 '/Users/frankie/.pyenv/versions/3.6.5/lib/python3.6',
 '/Users/frankie/.pyenv/versions/3.6.5/lib/python3.6/lib-dynload',
 '',
 '/Users/frankie/.pyenv/versions/3.6.5/lib/python3.6/site-packages',
 '/Users/frankie/.pyenv/versions/3.6.5/lib/python3.6/site-packages/IPython/extensions',
 '/Users/frankie/.ipython']

In [7]:

```

执行设置PYTHONPATH的命令后再重启python解释器之后就能正常导入foo了

```shell

export PYTHONPATH=/User/frankie
```

```shell

In [1]: import sys

In [2]: sys.path
Out[2]:
['/Users/frankie/.pyenv/versions/3.6.5/bin',
 '/User/frankie',
 '/Users/frankie/.pyenv/versions/3.6.5/lib/python36.zip',
 '/Users/frankie/.pyenv/versions/3.6.5/lib/python3.6',
 '/Users/frankie/.pyenv/versions/3.6.5/lib/python3.6/lib-dynload',
 '',
 '/Users/frankie/.pyenv/versions/3.6.5/lib/python3.6/site-packages',
 '/Users/frankie/.pyenv/versions/3.6.5/lib/python3.6/site-packages/IPython/extensions',
 '/Users/frankie/.ipython']

In [3]: import foo

In [4]: foo.hello()
hello
Out[4]: 'hello'



```





