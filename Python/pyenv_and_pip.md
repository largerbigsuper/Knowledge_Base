# Pyenv And Pip

## [pyenv](https://github.com/pyenv/pyenv) 

python多版本管理工具

一键安装脚本 [pyenv-installer](https://github.com/pyenv/pyenv-installer)

```shell
curl https://pyenv.run | bash
```

安装完成后还需要修改配置， bash用户修改.bashrc ,zsh用户修改.zshrc
```shell
echo 'export PATH="$HOME/.pyenv/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(pyenv init -)"' >> ~/.bashrc
echo 'eval "$(pyenv virtualenv-init -)"' >> ~/.bashrc
source ~/.bashrc
```

## [pyenv-virtualenv](https://github.com/pyenv/pyenv-virtualenv)

python虚拟环境管理工具

```shell
pyenv virtualenv <python版本> <环境名称>

pyenv activate <环境名称>
```


## 国内网速过慢解决办法

- python

[淘宝镜像](http://npm.taobao.org/mirrors/python)
将需要安装的压缩包下载至 `～/.pyenv/cache` 目录下，有时候cache目录并不存在需要手动创建。然后执行 `pyenv install <Python-version>`

```shell
mkdir -p ~/.pyenv/cache
http://npm.taobao.org/mirrors/python/$PYTHON_VERSION/Python-$PYTHON_VERSION.tar.xz -p ~/.pyenv/cache && pyenv install $PYTHON_VERSION && pyenv virtualenv $ENV_NAME

```

- pip

pip默认包源为python官方提供的地址，国内访问一般很慢，需要修改包源地址来提升下载速度

pip配置文件位置为 `~/.pip/pip.conf`,没有的话需要手动创建。然后将下面文本保存在pip.conf中。之后再pip install 就从阿里云提供的包源下载文件了。

```yaml
[global]
index-url = http://mirrors.aliyun.com/pypi/simple/
[install]
trusted-host = mirrors.aliyun.com

```





