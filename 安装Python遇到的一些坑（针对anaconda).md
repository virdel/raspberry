# 安装Python遇到的一些坑（针对anaconda)

新手学习python时，一般会选择安装anaconda包管理工具，而我们也是推荐这样做。

不过，在安装python之前，我们需要知道的是==anaconda里自带python==，也就是说你==不需要先安装python，再安装anaconda==。



如果你已经先安装了python，再安装了anaconda，必须注意你在cmd命令行模式输入python,启动的是你最先单独安装的python，在命令行模式下安装的包，也是安装在这个python里的。



如果使用anaconda下的python，你可以在Anaconda Prompt或着Anaconda Navigator 对包进行管理安装（你可以认为Anaconda Prompt是命令行版本，Anaconda Navigator是图形化版本）

![](https://upload-images.jianshu.io/upload_images/64542-4e9d1b7b08a5100e.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1000/format/webp)



### 虚拟环境

你可以把环境理解成盒子，不同的环境是不同的盒子，互相之间没有联系干扰。在不同的盒子里可以有自己单独的python编译器，也就是说你可以自己决定这些盒子具体的作用，如果你让环境1来做机器学习，就可以把与机器学习相关的包放在环境1里，如果你让环境2做 数据挖掘，就可以把相关的包放在环境2里。这些包是单独的，也就是说不同的环境可以有相同的包，他们是相互独立的。

如果你打开Anaconda Prompt，你会看到命令行前面有着（base),那就是anaconda初始的环境。



你可以在Anaconda Prompt里输入

``` 
conda  create -n python34  python=3.4
```

来创建名为python34的环境，命令中python34是环境的名称，3.4是环境里python的版本。



然后输入

```
activate python34
```

来切换到环境名为python34的环境。



如果你要安装包，一定要切换到相应的环境中安装。有时你在一个环境里安装了一个包，在另外一个环境里其实没有安装有这个包的，所以有时你在运行python时会有找不到的错误，就是因为没有正确地切换到该python的环境里安装包。



读完此文，你可以再读一读以下的文章：

​	[Anaconda完全入门指南](https://www.jianshu.com/p/eaee1fadc1e9)

​	[Jupyter Notebook介绍、安装及使用教程](https://www.jianshu.com/p/91365f343585)（针对Jupyter notebook的一系列的问题，强烈推荐）



在理解了以上的一些概念之后，使用anaconda就基本没什么问题了。