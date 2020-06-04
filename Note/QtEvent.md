## Qt Events

* 定义

  应用程序需要知道的，由应用程序内部或者外部产生的事情或者动作。



* 事件的处理

  1.重载paintEvent()，mousePressEvent()等时间处理函数。这是最常用也是最简单的方法，但是功能最有限。

  2.重载notify()函数，这个是最有效的，控制最全的方法，他可一存在于任何线程中，但是一次只能处理一个事件。

  3.在QCoreApplication的实例上install an event filter。这种方法和notify一样强大，但是因为需要全局的event filter。这也导致他只能存在于主线程。

  4.重载event()，这个函数会在任何widget-specific event filters函数之前触发。

  5.在对象上install an event filter，这个event filter可以获取所有的events，包括tab和shift+Tab的key press events，当然他无法改变当前widget的焦点。



​		总结：实际编程中最常用的是方法1，其次是方法5，方法2和3虽然功能很强大，但是2需要继承QApplication类，3需要全局的event filter，将减缓事件的传递。



* 时间的传递顺序
  * 时间过滤器
  * 焦点部件的event函数
  * 焦点部件的时间处理函数
  * 如果焦点忽略了该事件，就执行父部件的事件处理函数。