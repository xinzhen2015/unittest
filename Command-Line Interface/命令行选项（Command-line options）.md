## Command-line options
***
unittest支持以下命令行选项参数：

### -b，--buffer  

标准输出和标准错误流在测试运行期间被缓冲（记录）。输出中执行通过的测试将被丢弃，当测试失败或报错时，输出通常会有回应，并被记录在失败消息中。

### -c, --catch

在测试执行的过程中敲入 contral + c，则当前测试结束后，生成目前为止的所有测试结果。

### -f， --failfast

执行测试的过程中，遇到第一个报错或者断言失败就停止测试

### -k

只运行与模式或子字符串匹配的测试方法和类。这个选项可以多次使用，在这种情况下，所有与给定模式匹配的测试用例都包括在内。

使用fnmatch.fnmatchcase()将包含通配符(*)的模式与测试名称匹配;另外，也可以使用简单的区分大小写的子字符串做匹配。

例如：

-k foo matches foo_tests.SomeTest.test_something, bar_tests.SomeTest.test_foo, ***but not*** bar_tests.FooTest.test_something.

### --locals

在错误信息追踪里展示本地变量

Version 3.2新增：-b,-c,-f  
Version 3.5新增：--locals  
Version 3.7新增：-k  

命令行还可以用于测试发现，在项目中运行所有测试或只是一个子集。
