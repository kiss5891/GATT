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

>>>>>>> fce5e5b6c1c7a4a990c809c7101dac4212b78908
