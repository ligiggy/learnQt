# Qt笔记

## 知识点

* VS中如何显示汉字，在头文件中加入

  ~~~
  #if defined(_MSC_VER) && (_MSC_VER >= 1600)    
  # pragma execution_character_set("utf-8")    
  #endif
  ~~~



* 如果是用Qt Creator，在加上Q_Object宏之后报错，需要将MakeFile文件删除，再重新编译，就不会报错了。



* Qt Buddy模式

  就是在buddy模式下，在标签上加上&，然后连接标签和对应控件，那么alt+&后面的字母，就可以将焦点移动到设置的控件上。

  加速键与快捷键有区别，快捷键不需要获取焦点。



* Qt排序Tab

  选择Tab模式，鼠标左键单击即可排序。



* F3退出当前设计的模式。（比如Buddy模式）



## 问题

* VS中，connect函数已经在setupUi()函数中实现了，不需要再自己写代码将其连接起来。

