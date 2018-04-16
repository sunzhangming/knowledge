# python3中pip的指向问题
* [参考资料](https://blog.csdn.net/u012516318/article/details/75339860)
#### 问题描述
> 在centos7系统上，同时安装了python2与python3
> 在使用python3的时候报错No module  name requests,所以应该是python3中没有这个模块
> 按常理出牌，使用`pip3 install requests`
> ![enter description here](./images/1523627867804.jpg)
> 很明显
> `You are using pip version 8.1.1, however version 9.0.3 is available.
You should consider upgrading via the 'pip install --upgrade pip' command.`这个错误应该升级pip嘛，但是
> `Requirement already up-to-date: pip in /usr/local/lib/python2.7/site-packages`
>喏，显示这个，很容易发现我想要的是python3，他怎么给我显示python2呢，好，你不仁就别怪我无义了，霸王硬上弓，把pip的软连接指向python3就万事大吉了。
>命令如下：which pip

* 一般情况下会显示：

> `/usr/local/bin/pip`

* 然后 `vim /usr/local/bin/pip`

>我们可以看到如下：

> `#!/usr/bin/python`

* 将第一行 #!/usr/bin/python3 修改为

> `#!/usr/bin/python2`

然后pip 就指向python3了