
Google leveldb in windows for Visual Studio 2013

[原项目地址](https://github.com/bureau14/leveldb)

这里是基于这个项目使用VS2013建立的一个 Console 应用程序，如果需要编译为静态库，直接修改项目属性即可。鉴于各种版本的库下载下来都不能直接用，需要各种设置修改，此处备份一个可以直接使用的项目。

leveldb需要使用boost库，下载官方boost源码，按说明编译即可。boost的编译说明和编译方式非常人性话，基本按说明就可以编译成功。boost目录和项目处于同级目录，如果不是，需要修改项目的boost路径设置。

LevelDB qdb branch
==================

Current version: 1.18

quasardb [LevelDB](http://code.google.com/p/leveldb/) branch with full Windows support. This is not an official LevelDB branch, but the branch we use in our product, [quasardb](https://www.quasardb.net/).

* Full Windows support: everything builds, all tests pass;
* [CMake](http://www.cmake.org/) based build
* Explicit (thread unsafe) de-allocation routines for "clean exits". Helps a lot when running your application into a leak detector;
* The Windows build requires [Boost](http://www.boost.org/); 
* Our code is C++11ish and may require a recent compiler;
* Lots of warnings fixed;
* Is not 100% compliant with Google coding style.

Tested on [FreeBSD](http://www.freebsd.org/), Linux and Windows (32-bit & 64-bit).

Might contains trace of nuts.

Comments? Questions? Suggestions? Pull!
