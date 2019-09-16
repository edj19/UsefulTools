Simulations
===============
That has a paragraph about a main subject and is set when the '='
is at least the same length of the title itself.
 
Molecular Dynamics
---------------------
Subtitles are set with '-' and are required to have the same length 
of the subtitle itself, just like titles.
 
Lists can be unnumbered like:
 
 * Item Foo
 * Item Bar
 
Or automatically numbered:
 
 #. Item 1
 #. Item 2
 
ROOT-Data Analysis Framework
------------------------------
Root is a modular scientific software toolkit.It provides all the functionalities needed to
deal with big data processing,statistical analysis,visualisation and storage.It is mainly written
in C++ but integrated with other lanuages such as Python and R.

Installing the Root 
^^^^^^^^^^^^^^^^^^^^^^^

**Build Prerequisites**
This page lists the Prerequisites packages that need to be install on the Ubuntu systems where 
you can use the following commands.

Required packages:

sudo apt-get install git dpkg-dev cmake g++ gcc binutils libx11-dev libxpm-dev \
libxft-dev libxext-dev

Optional packages:

sudo apt-get install gfortran libss1-dev libpcre3-dev \
xlibmesa-glu-dev libglew1.5-dev libftg1-dev \
libmysqlclient-dev libfftw3-dev libcfitsio-dev \
graphviz-dev libavahi-compat-libdnssd-dev \
libldap2-dev python-dev libxml2-dev libkrb5-dev \
libgs10-dev libqt4-dev


1. Download the source code<https://root.cern.ch/downloading-root>
2. tar -zxvf root_v6.18.04.source.tar.gz
3. mkdir build(obj)
4. cd build(obj)
5. cmake ../root-6.18.04
6. make -j n
7. Add the path/build(obj)/bin.thisroot.sh to the .bashrc file and source .bashrc file

Getting started
^^^^^^^^^^^^^^^^^^

Root的基本语法可以参考官网，官网也是上手最快、获取帮助最直接的地方；此外大家记得将root目录下的tutorials
文件夹拷贝到特定的root学习文件夹，比如root_task目录下，因为这里面的好多例子是需要我们结合自己的
研究情况或者作图方式要时刻去参考的，大家要随时去查阅相关命令。

好了接下来开始我们的root学习之旅，无论你学习root的出发点是什么，我相信它必定会变成你一款未来你爱不释手的
工具，接下来我主要重点讲解root应用的几个方面：

1. root脚本

一听到脚本是不是大家像我一样感到兴奋呢，无论是shell脚本、python脚本或者root脚本，反正我听到我就感觉上瘾了！
首先当你安装好root后，运行脚本的命令非常简单：
root -l script.C

是不是感觉很方便，你可以在script.C中安装C++的语法和root的基本语法，实现任何你想实现的东西，感觉自己又可以复习
C++了，那就简单编写一个：

.. code-block:: c
    :linenos:

    {
        cout<<"Hello ROOT"<<endl;
        int Num=5;
        for(int i=0;i<Num;i++)
        {
            cout<<"root i="<<i<<endl;
        }
    }

然后将上述文件保存为ex00.C后运行root -l ex00.C就会出现相应的结果。是不是非常简单，那就尝试编写更多的
root脚本文件开展工作吧。








Geant4 
----------

Installation
^^^^^^^^^^^^^^^

1. 安装cmake.
2. 安装必须的库:
sudo apt-get libgl1-mesa-dev libglu1-mesa-dev libxt-dev \
libXmu-dev libXi-dev zlib1g-dev libgl2ps-dev \
libexpat1-dev libxerces-c-dev.
3. 下载安装文件，下载Source files 和 Data files.
4. 建立目录Geant4,并在目录下建立geant4-build,geant4-install,geant4-projects分别编译、运行和项目的目录，
然后将Source file解压在该文件目录下，最终文件目录结构如下
ant4--[geant4.10.05,geant4-build,geant4-install,geant4-projects].
5. cd geant4-build.
6. cmake -DCMAKE_INSTALL_PREFIX=/PATH/geant4-install -DGEANT4_USE_OPENGL_X11=ON \
-DGEANT4_BUILD_MULTITHREADED=ON -DGEANT4_USE_RAYTRACER_X11=ON \
-DGEANT4_USE_GDML=ON ../geant4.10.05.
7. make -jN.
8. make install.
9. 设置环境变量：为了可以使用Geant4 Library,我们需要设置相应的环境变量，将所有的Library文件路径添加到
系统环境变量中.

Getting started
^^^^^^^^^^^^^^^^
**运行例子**：接下来我们就可以运行Geant4提供的例子运行并学习修改，其中geant4.10.05/examples/里面的
basic中的例子最为简单，供入门学习，接下来我们先运行B1例子为例进行讲解：

1. 将B1例子拷贝到我们前面建立的geant4-projects中(对于后面的项目也类似)；
2. cd geant4-projects/example;
3. mkdir build;
4. cmake -DGeant_DIR=/path_to_geant4-install/lib/Geant4-10.5.0 ../;
5. make -jN;
6. ./example;

**编译器选择**：作为神器编译器，当然推荐Visual Studio Code了，当然安装也是非常简单的：

1. 下载.deb文件
2. sudo dpkg -i code_1.deb   
3. sudo apt-get -f install
4. 然后你就可以在应用程序中找到它了，打开后将你的项目文件导入进去就好.
5. 在你导入文件后，你会发现有许多报错语句#include" .hh",这是点击报错语句前的“小灯泡”，
选择Edit includePath Setting,这是打开c_cpp_properties.json文件，修改其中的“includePath",在后面添加
相应的头文件的路径就好."/home/day/materials/Geant4/geant4-projects/B1/include","/home/day/materials/Geant4/geant4-install/include/Geant4".

Basics of Monte Carlo Simulation

 * Historical review of Monte Carlo methods
 * Basics of Monte Carlo method
 * Two Monte Carlo particle transport examples
 * Boosting Simulation
 * A partial list of Monte Carlo codes