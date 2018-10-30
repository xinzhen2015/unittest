# unnitest 中文文档 （Unit testing framework）
***

unittest 框架中文文档，起因是看到官方文档有English、French、Japanese、Korean，唯独没有Chinese，这就很不爽了。  

🇨🇳  
本文：尊重原创，翻译遵循信达雅。   
🇨🇳   

Python版本：3.7.1

[unittest官方英文文档](https://docs.python.org/3/library/unittest.html#test-discovery)
***

# unnitest--单元测试框架
## Source code：[Lib/unittest/__init__.py](https://github.com/python/cpython/blob/3.7/Lib/unittest/__init__.py)  

(亲爱的，如果你对测试概念已经有所了解，请直接跳到 [断言方法列表](https://docs.python.org/3/library/unittest.html#assert-methods)。🌹)

unittest 单元框架最初的灵感来自于JUnit，它和其他语言中的单元测试框架有着相似的韵味。例如它支持自动化测试、共享测试的设置和关闭代码、将测试聚合到集合中，以及测试与报告框架的独立性。  

为此，unittest以面向对象的方式支持如下概念：

**测试夹：**

```
注：测试夹（Fixture） 指的是测试中依赖的数据和条件等等，unittest提供对Fixture的支持。
```
测试夹是指执行一个或多个测试任务所需要的准备工作，以及任何相关联的清理操作。这可能包括，例如，创建临时或代理数据库、创建目录或启动服务器进程。

**测试用例：**

一个测试用例是一个独立的单元测试，它检查对特定输入集的特定响应。unittest提供了一个基类（[TestCase](https://docs.python.org/3/library/unittest.html#unittest.TestCase)），能够用他去创建新的测试用例。

**测试套件：**  

测试套件是测试用例或者测试套件本身的集合，也可以是测试用例和测试套件的混合集合，它把要执行的测试汇聚起来。  

**测试运行器**  

测试运行器是用于编排测试用例，以及向用户展示测试结果。运行器可以使用图形界面、文本界面，或者是返回特定的值去展示执行后的测试结果。

```
请参阅：
doctest模块(https://docs.python.org/3/library/doctest.html#module-doctest)：另外一种具有独特韵味的测试支持模块。
```


