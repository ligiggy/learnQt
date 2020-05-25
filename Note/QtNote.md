# Qt笔记

## 知识点

* VS中如何显示汉字，在头文件中加入

  ~~~
  #if defined(_MSC_VER) && (_MSC_VER >= 1600)    
  # pragma execution_character_set("utf-8")    
  #endif
  ~~~



* 如果是用QtCreator，在加上Q_Object宏之后报错，需要将MakeFile文件删除，再重新编译，就不会报错了。



## 问题

* VS中，connect函数已经在setupUi()函数中实现了，不需要再自己写代码将其连接起来。

