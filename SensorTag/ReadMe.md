#Debug 因為他切程了兩個檔案所以要兩個一起燒錄
Because the workspace is split into two projects (application and stack), the following is the specific sequence for compilation and download.
#step
1. Set the application project as the active project.
2. Select Project → Build All to build the project.
3. Set the stack project as the active project.
4. Select Project → Build All to build the project.
5. Select the application project as the active project.
6. Select Run → Debug to download the application.
7. Select the stack project as the active project.
8. Select Run → Debug to download the stack.<br>
By (http://www.ti.com.cn/cn/lit/ug/swru393b/swru393b.pdf)

***
![yuml.me](http://yuml.me/e284bdd4)
___
![jpg](./img/SensorTag.jpg)

<<<<<<< HEAD
'''flow 
start

'''
=======

#add system_printf

Here main steps (for TI BLE stack applications):

1) Modify your appBLE.cfg config file (e.g. CCS > Project Explorer > YourApp > TOOLS > appBLE.cfg)
var System = xdc.useModule('xdc.runtime.System');
var SysStd = xdc.useModule('xdc.runtime.SysStd');
System.SupportProxy = SysStd;
System.SupportProxy = SysCallback; > System.SupportProxy = SysStd;

2) Add SysStd variable

SysStd = xdc.useModule("xdc.runtime.SysStd");

3) Open main module (e.g. CCS > Project Explorer > YourApp > Startup > main.c) and add
```C
#include <xdc/runtime/System.h>
```
...

System_printf("TEST\n");
