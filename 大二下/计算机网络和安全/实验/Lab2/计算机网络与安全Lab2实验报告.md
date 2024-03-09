#  计算机网络与安全Lab2实验报告

*李思全*

*22307130049*

## 1.**基本HTTP GET/response交互**

1. 您的浏览器是否运行HTTP版本1.0或1.1？服务器运行什么版本的HTTP？

   运行版本HTTP/1.1：![image-20240305111341018](C:\Users\pc\AppData\Roaming\Typora\typora-user-images\image-20240305111341018.png)

2. 您的浏览器会从接服务器接受哪种语言（如果有的话）？

   text/html语言：![image-20240305111500987](C:\Users\pc\AppData\Roaming\Typora\typora-user-images\image-20240305111500987.png)

3. 您的计算机的IP地址是什么？ gaia.cs.umass.edu服务器地址呢？

   我的计算机IP：10.223.209.1

   gaia.cs.umass.edu服务器地址：128.119.245.12

   ![image-20240305111806357](C:\Users\pc\AppData\Roaming\Typora\typora-user-images\image-20240305111806357.png)

4. 服务器返回到浏览器的状态代码是什么？

   200 OK：![image-20240305111902590](C:\Users\pc\AppData\Roaming\Typora\typora-user-images\image-20240305111902590.png)

5. 服务器上HTML文件的最近一次修改是什么时候？

   2024 Mar 04 06:59:02：![image-20240305112341198](C:\Users\pc\AppData\Roaming\Typora\typora-user-images\image-20240305112341198.png)

6. 服务器返回多少字节的内容到您的浏览器？

   128 bytes：![image-20240305112506571](C:\Users\pc\AppData\Roaming\Typora\typora-user-images\image-20240305112506571.png)

## 2.**HTTP条件Get/response交互**

7. 检查第一个从您浏览器到服务器的HTTP GET请求的内容。您在HTTP GET中看到了"IF-MODIFIED-SINCE"行吗？

   没有

8. 检查服务器响应的内容。服务器是否显式返回文件的内容？ 你是怎么知道的？

   是的：![image-20240305115540297](C:\Users\pc\AppData\Roaming\Typora\typora-user-images\image-20240305115540297.png)可以看到此处有着显式的html文件

9. 现在，检查第二个HTTP GET请求的内容。 您在HTTP GET中看到了"IF-MODIFIED-SINCE:"行吗？ 如果是，"IF-MODIFIED-SINCE:"头后面包含哪些信息？

   看到了，包含了最近修改的时间：![image-20240305115749743](C:\Users\pc\AppData\Roaming\Typora\typora-user-images\image-20240305115749743.png)

10. 针对第二个HTTP GET，从服务器响应的HTTP状态码和短语是什么？服务器是否明确地返回文件的内容？请解释。

    状态码是304，短语Not Modified，不明确返回文件内容，因为在上一次请求中已经得到了最近修改的文件，只需从缓存中访问即可，不需再次返回：![image-20240305120124146](C:\Users\pc\AppData\Roaming\Typora\typora-user-images\image-20240305120124146.png)

## **3.具有嵌入对象的HTML文档**

11. 您的浏览器发送了几个HTTP GET请求消息？ 这些GET请求发送到哪个IP地址？

    发送了三个HTTP GET请求消息，分别发送到： 128.119.245.12 128.119.245.12 178.79.137.164<img src="C:\Users\pc\AppData\Roaming\Typora\typora-user-images\image-20240305120434154.png" alt="image-20240305120434154" style="zoom:25%;" />

12. 浏览器从两个网站串行还是并行下载了两张图片？请说明

    串行下载：可以看到浏览器在接收到第一张图片的返回信息后才开始请求第二张图片![image-20240305120719617](C:\Users\pc\AppData\Roaming\Typora\typora-user-images\image-20240305120719617.png)

## **4.HTTP认证** 

13.  对于您的浏览器的初始HTTP GET消息，服务器响应（状态码和短语）是什么响应？

    状态码是401，短语是unauthorized：![image-20240305121139299](C:\Users\pc\AppData\Roaming\Typora\typora-user-images\image-20240305121139299.png)

14.  当您的浏览器第二次发送HTTP GET消息时，HTTP GET消息中包含哪些新字段？

    包含了新字段“Cache-Control”和“Authorization”：![image-20240305121514975](C:\Users\pc\AppData\Roaming\Typora\typora-user-images\image-20240305121514975.png)

    