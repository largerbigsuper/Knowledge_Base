# isntall tensorflow

## 创建一个python3.6.5 的名为tensorflow的虚拟环境

```shell
export PYTHON_VERSION=3.6.5
export ENV_NAME=tensorflow

wget http://npm.taobao.org/mirrors/python/$PYTHON_VERSION/Python-$PYTHON_VERSION.tar.xz -P ~/.pyenv/cache && \
pyenv install $PYTHON_VERSION && \
pyenv virtualenv $PYTHON_VERSION $ENV_NAME &&\
pyenv activate $ENV_NAME

```

## 安装tensorflow

参考文档 `https://www.tensorflow.org/install`

```shell

pip install --upgrade pip

pip install --upgrade tensorflow
```

## 测试安装

```
python -c "import tensorflow as tf; tf.enable_eager_execution(); print(tf.reduce_sum(tf.random_normal([1000, 1000])))"

```

## 问题

- `I tensorflow/core/platform/cpu_feature_guard.cc:141] Your CPU supports instructions that this TensorFlow binary was not compiled to use: AVX2 FMA`

我们的CPU支持未编译此TensorFlow二进制文件的指令：AVX2 FMA

