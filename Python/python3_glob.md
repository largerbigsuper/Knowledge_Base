# Python3 - glob

[glob — Unix style pathname pattern expansion](https://docs.python.org/3/library/glob.html)

```python

# 获取当前目录下的所有py文件, recursive参数并不起作用
glob.glob('*.py', recursive=True)

# 获取当前目录下所有文件夹下的py文件, **匹配所有文件
glob.glob('**/*.py', recursive=True)

# simple目录下所有文件的获取绝对路径
glob.glob('/Users/frankie/Projects/simple/**', recursive=True)

```

```python

"""
➜  Projects tree simple
simple
├── Dockerfile
├── __pycache__
│   └── app.cpython-36.pyc
├── app.py
├── docker-compose.debug.yml
├── docker-compose.yml
├── gunicorn.py
├── logs
│   ├── access.log
│   ├── app.log
│   └── error.log
├── requirements.txt
├── run.sh
└── supervisord.conf

2 directories, 12 files
➜  Projects pwd
/Users/frankie/Projects
"""

import os
import glob

In [7]: os.chdir('/Users/frankie/Projects/simple')

In [8]:  glob.glob('**', recursive=True)
Out[8]:
['__pycache__',
 '__pycache__/app.cpython-36.pyc',
 'app.py',
 'docker-compose.debug.yml',
 'docker-compose.yml',
 'Dockerfile',
 'gunicorn.py',
 'logs',
 'logs/access.log',
 'logs/app.log',
 'logs/error.log',
 'requirements.txt',
 'run.sh',
 'supervisord.conf']

In [9]: glob.glob('/Users/frankie/Projects/simple/**', recursive=True)
Out[9]:
['/Users/frankie/Projects/simple/',
 '/Users/frankie/Projects/simple/__pycache__',
 '/Users/frankie/Projects/simple/__pycache__/app.cpython-36.pyc',
 '/Users/frankie/Projects/simple/app.py',
 '/Users/frankie/Projects/simple/docker-compose.debug.yml',
 '/Users/frankie/Projects/simple/docker-compose.yml',
 '/Users/frankie/Projects/simple/Dockerfile',
 '/Users/frankie/Projects/simple/gunicorn.py',
 '/Users/frankie/Projects/simple/logs',
 '/Users/frankie/Projects/simple/logs/access.log',
 '/Users/frankie/Projects/simple/logs/app.log',
 '/Users/frankie/Projects/simple/logs/error.log',
 '/Users/frankie/Projects/simple/requirements.txt',
 '/Users/frankie/Projects/simple/run.sh',
 '/Users/frankie/Projects/simple/supervisord.conf']


```