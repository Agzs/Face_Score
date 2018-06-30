# Face_Score

### Environment configuration

```
Virtual box 5.1.30 r118389，Ubuntu 16.04，64 位。
PYTHON2.7，Tensorflow 版本 1.4，无其它依赖库。
```

1) install python-pip & python-dev
```sh
sudo apt-get install python-pip python-dev
```

2) install tensorflow version 1.4.0
```sh
sudo pip install --upgrade https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow-1.4.0-cp27-none-linux_x86_64.whl
```

3) test tensorflow
```python
aguan@aguan:~$ python
Python 2.7.12 (default, Dec  4 2017, 14:50:18) 
[GCC 5.4.0 20160609] on linux2
Type "help", "copyright", "credits" or "license" for more information.
>>> import tensorflow as tf
>>> hello=tf.constant('hello')
>>> sess=tf.Session()
2018-06-30 13:20:52.439142: I tensorflow/core/platform/cpu_feature_guard.cc:137] Your CPU supports instructions that this TensorFlow binary was not compiled to use: SSE4.1 SSE4.2 AVX
>>> print(sess.run(hello))
hello
>>> a=tf.constant(10)
>>> b=tf.constant(32)
>>> print(sess.run(a+b))
42
>>> exit()
```

4) run
```
mkdir model

python face_train.py

copy new files to model

python face_test.py
```
