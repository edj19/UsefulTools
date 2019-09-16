Calculations
===============
That has a paragraph about a main subject and is set when the '='
is at least the same length of the title itself.
 
Python Problems
----------------
Sometimes we may suffer some problems of python intepreters in Ubuntu system.And we should know
how to change python intepreter.我们使用update-alternatives来为整个系统更改python默认版本

具体命令`a link`：

.. _a link: https://blog.csdn.net/ycy_dy/article/details/80869271

 * sudo update-alternatives --list python
 * ls -l /usr/bin/python /usr/bin/python3
 * sudo update-alternatives --install /usr/bin/python python /usr/bin/python2.7 1
 * sudo update-alternatives --install /usr/bin/python python /usr/bin/python3.6 2
 * sudo update-alternatives --list python
 * sudo update-alternatives --config python


 
Lists can be unnumbered like:
 
 * Item Foo
 * Item Bar
 
Or automatically numbered:
 
 #. Item 1
 #. Item 2
 
