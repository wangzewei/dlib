安装dlib本身就难： 笔者花了一天的时间尝试了官网和非官网的N种上述主流方法，都会出现dlib安装编译错误。最后采用了一种非主流方法，成功安装dlib，
首先，如果你是第一次使用Face_recogintion,前提是必须要知道以下依赖关系：

'''
Win下python3.6版本：

1. 安装face_recongnition的必要条件是：配置好Dlib和openCV

2. 安装Dlib的必要条件是： 配置好boost和cmake

'''
注意：请务必从最底层的依赖项目开始进行安装

在没有安装好第二步之前，不要安装dlib

在没有安装好dlib之前，不要进行安装face_recongnition。

安装的所有的文件都在python的安装路径下的lib文件夹下。
开始安装



###第一步：

首先，你需要下载一个python的编译环境，我所使用的是python3.6版本。

系统配置为win10，64位。在安装时选择能够匹配自己电脑系统的既可以。

注意：选择安装路径默认生成。

如果在2.7的版本下，可以记得需要选择pip工具。

然后，一直选择下一步，进行安装，等待安装成功就可以了。

安装方式和语法详情，小白专用：廖雪峰官网



###第二步：

组合键：win+R  输入cmd

然后使用回车进入，输入python就可以看到自己的版本了。

显示下面的内容就代表已经安装成功了。



###第三步：

我们开始一层一层的进行安装

（1）先安装Cmake和boost

在CMD下输入以下内容：

输入pip  install  cmake ，回车，安装

输入pip  install  boost ，回车，安装

如果网络正常，显示安装不上的，请移步到文末尾。

仅显示一个安装成功界面，下面相同类似。



###第四步：（关键）

（2）安装dlib，此处有大坑。脱坑方法如下

https://github.com/wangzewei/dlib

点击这个链接，然后选择适合你自己的delib文件

然后将其放到C盘的根目录下，然后进入到CMD下

然后输入pip install  文件名

等待安装完成就可以了。

显示界面同第三步所示。



###第五步:

（3）安装opencv和face_recongnition

因为face_recongnition一般要配合opencv的使用

所以在这里我们将opencv和face_recongnition都进行安装。

输入pip  install  opencv-python ，回车，安装

输入pip  install  face_recongnition，回车，安装

显示界面同第三步所示。



####验证

在命令行下输入python，进入界面后。输入：

import   模块名称

如果没有出现报错的现象就可以说明已经安装成功了。

举例：将下面的内容依次输入测试ok，就说明安装已经成功了。

import    cmake            

import    boost                                

import   cv2                                       //opencv-python的验证是cv2

import    face_recongnition

import    dlib



####数坑

###问题1：黄色的在字体部分

处理：你需要下载最新版本的pip

在CMD下输入：python -m pip install --upgrade pip，回车，等待安装完成。



###问题2：红色的字体的部分


处理：你需要下载与你的版本匹配的dlib

重新选择匹配自己电脑和python版本的的dlib



###问题3：白色的字体的部分


处理：请重新检查输入的命令是不是有错



####问题3：白色的字体的部分


处理：你已经安装过这个库了，不需要重新安装。



####结束语：

'''

复习一下：

1.安装python3.6

2.安装opencv和face_recongnition

3.验证

然后就可以使用pythonIDE下使用opencv和face_recongnition了。
'''
