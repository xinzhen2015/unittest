# unnitest 中文文档 （Unit testing framework）
***
unittest 框架中文文档，起因是看到官方文档有English、French、Japanese、Korean，唯独没有Chinese，这就很不爽了。  

本文：尊重原创，严格对重官方文档，翻译遵循信达雅。 

Python版本：3.7.1

[unittest官方英文文档](https://docs.python.org/3/library/unittest.html#test-discovery)
***

# unnitest--单元测试框架
## Source code：[Lib/unittest/__init__.py](https://github.com/python/cpython/blob/3.7/Lib/unittest/__init__.py)  

(亲爱的，如果你对测试概念已经有所了解，请直接跳到 [断言方法列表](https://docs.python.org/3/library/unittest.html#assert-methods)。🌹)

unittest 单元框架最初的灵感来自于JUnit，它和其他语言中的单元测试框架有着相似的韵味。例如它支持自动化测试、共享测试的设置和关闭代码、将测试聚合到集合中，以及测试与报告框架的独立性。  

为此，unittest以面向对象的方式支持如下概念：

**测试夹**

```
注：测试夹（Fixture） 指的是测试中依赖的数据和条件等等，unittest提供对Fixture的支持。
```
测试夹是指执行一个或多个测试任务所需要的准备工作，以及任何相关联的清理操作。这可能包括，例如，创建临时或代理数据库、创建目录或启动服务器进程。

**测试用例**
