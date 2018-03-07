###【Python】 Missing parentheses in call to 'print'
- 问题描述： 一直用pycharm在运行python脚本，今天打开了python自带的idle.bat(路径为C:\Python35\Lib\idlelib)，打开之后直接用print “hello world”报错，错误信息：SyntaxError: Missing parentheses in call to 'print'
- 解决方案：python2系列可以支持print 'xxx';python3系列支持的是print('xxx');计算机上装的是python3；使用后者即可运行成功
