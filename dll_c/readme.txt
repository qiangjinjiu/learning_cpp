参考网址
https://blog.csdn.net/vivianke/article/details/6994013
https://www.linuxidc.com/Linux/2011-02/32453.htm


编译为dll
gcc test_a.c -fPIC -shared -o libtest.dll

-o的参数指定的动态库的名字需要为libxxx.dll

运行
gcc test.c -L. -ltest -o test

参数说明：
-fPIC：示生成地址无关代码，
-shared：指示生成动态链接库 
-L：表示要连接的库在当前目录中，
-ltest：编译器查找动态连接库时有隐含的命名规则，即在给出的名字前面加上lib，后面加上.dll(Cygwin)（Linux环境中是.so）来确定库的名称

运行效果：
$ ./test.exe
this is in test_a...
