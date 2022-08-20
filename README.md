# 2022年夏季《移动软件开发》实验报告



<center>姓名：叶鹏  学号：20020007095</center>

| 姓名和学号         | 叶鹏，20020007095                                            |
| ------------------ | ------------------------------------------------------------ |
| 本实验属于哪门课程 | 中国海洋大学22夏《移动软件开发》                             |
| 实验名称           | 实验3：视频播放小程序                                        |
| 博客地址           | [Click me if you can](http://existot01.top/)                 |
| Github仓库地址     | [You won't miss that](https://github.com/ExistoT01/mobileSoftwareDesign-lab2) |

（备注：将实验报告发布在博客、代码公开至 github 是 **加分项**，不是必须做的）



## **一、实验目标**

- 掌握视频列表的切换方法
- 掌握视频自动播放方法
- 掌握视频随机颜色弹幕效果

## 二、实验步骤

列出实验的关键步骤、代码解析、截图。

1. 项目创建

   <img src="C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20220819204135596.png" alt="image-20220819204135596" style="zoom:80%;" />

2. 页面配置

   <img src="C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20220819204257141.png" alt="image-20220819204257141" style="zoom:80%;" />

3. 视图设计

   1. 导航栏设计

      <img src="C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20220819204529523.png" alt="image-20220819204529523" style="zoom:80%;" />

      <img src="C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20220819204540151.png" alt="image-20220819204540151" style="zoom:80%;" />

   2. 页面设计

      1. 区域1：视频播放器

         <img src="C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20220819205937346.png" alt="image-20220819205937346" style="zoom:80%;" />

         <img src="C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20220819205946243.png" alt="image-20220819205946243" style="zoom:80%;" />

      2. 区域2：弹幕发送区域

         <img src="C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20220819210001765.png" alt="image-20220819210001765" style="zoom:80%;" />

         <img src="C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20220819210009622.png" alt="image-20220819210009622" style="zoom:80%;" />

      3. 区域3：视频列表

         <img src="C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20220819211352742.png" alt="image-20220819211352742" style="zoom:80%;" />

         <img src="C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20220819211406321.png" alt="image-20220819211406321" style="zoom:80%;" />

4. 逻辑实现

   1. 更新播放列表

      <img src="C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20220819212349084.png" alt="image-20220819212349084" style="zoom:80%;" />

      <img src="C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20220819212357305.png" alt="image-20220819212357305" style="zoom:80%;" />

   2. 点击播放视频

      <img src="C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20220820143127802.png" alt="image-20220820143127802" style="zoom:80%;" />

      <img src="C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20220820143554348.png" alt="image-20220820143554348" style="zoom:80%;" />
   
   3. 发送弹幕
   
      <img src="C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20220820145602656.png" alt="image-20220820145602656" style="zoom:80%;" />
   
      <img src="C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20220820145630763.png" alt="image-20220820145630763" style="zoom:80%;" />
   
      
   

## 三、程序运行结果

列出程序的最终运行结果及截图。

<img src="C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20220820145647379.png" alt="image-20220820145647379" style="zoom:80%;" />

<img src="C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20220820145713542.png" alt="image-20220820145713542" style="zoom:80%;" />



## 四、问题总结与体会

本次实验中学习到了视频播放器的一些使用，对于本实验我觉得存在一些不严谨的地方

- `vx:key`元素指定不明确

<img src="C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20220820145920418.png" alt="image-20220820145920418" style="zoom:80%;" />

​	实验自始至终未指定`video{{index}}`到底指的是什么

- 未介绍`videoContext`对象

​	实验中只是展示但是没有解释`wx.createVideoContext`函数，这个函数是创建一个视频播放器对象，创建的对象我们取名未`videoCtx`，它自身包含有`Play()`和`Stop()`内置函数

- 部分变量不包含在页面初始数据内

​	如`src`，`videoCtx`，未在`Page`的`data`内声明，而是由一些别的函数生成，不知道是否严谨