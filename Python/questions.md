# Python3常见问题


## `'ascii' codec can't encode characters in position 34-40: ordinal not in range(128)`

python3输出编码的问题

[Python3—UnicodeEncodeError 'ascii' codec can't encode characters in position 0-1](https://blog.csdn.net/AckClinkz/article/details/78538462)


解决办法：

```shell
# 1.执行python3脚本时，添加额外参数
PYTHONIOENCODING=utf-8 python your_script.py

# 设置环境变量

export PYTHONIOENCODING=utf-8

python your_script.py

```

