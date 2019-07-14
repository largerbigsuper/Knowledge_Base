# supervisord

python 进程管理工具


## bugs


%(ENV_)获取环境变量的值是supervisord启动时的环境变量。之后通过export修改变量的值是不起作用的。只用把supervisord重启才可以加载到新的变量的值。

```
supervisorctl -c supervisord.conf shutdown
suprvisord -c supervisord.conf

```


```shell
[program:example]
command=/usr/bin/example --loglevel=%(ENV_LOGLEVEL)s
```