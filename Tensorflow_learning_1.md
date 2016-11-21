### Tensorflow 介绍
Tensorflow是Google发布的人工智能系统.
软件可以从大量数据来判断未来情况的趋势.
英文官方网站：
http://tensorflow.org/

官方GitHub仓库：
https://github.com/tensorflow/tensorflow

中文版 GitHub 仓库：
https://github.com/jikexueyuanwiki/tensorflow-zh

### Tensorflow 安装
Tensorflow本身是基于python2/3平台,所以可以直接通过pip进行安装
- 建立虚拟环境virtualenv 

`$ virtualenv -p /usr/local/bin/python3.5 Env3.5`
- 启动虚拟环境

`$ source Env3.5/bin/activate`
- 导入安装库(oxs如果没有安装CUDA,只能通过CPU安装)

```
# Mac OS X, CPU only, Python 3.4 or 3.5:
$ export TF_BINARY_URL=https://storage.googleapis.com/tensorflow/mac/cpu/tensorflow-0.11.0rc1-py3-none-any.whl
```
- 安装tensorflow


```
# Python 3
$ pip3 install --upgrade $TF_BINARY_URL
```
- 测试Tensorflow
```
$ python
>>> import tensorflow as tf
>>> hello = tf.constant('Hello, TensorFlow!')
>>> sess = tf.Session()
>>> print(sess.run(hello)) Hello, TensorFlow!
>>> a = tf.constant(10)
>>> b = tf.constant(32)
>>> print(sess.run(a + b)) 42
```

至此 Tensorflow安装成功