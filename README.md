# movie-ticke

### 一、目的

通过制作一个电影院售票界面来掌握使用   HTML、CSS、JAVASCRIPT及jQuery框架等网页前端开发语言。

### 二、要求

实现影院订票前端页面，如图1-1所示。要求具有以下主要功能：

1．一次最多仅能选中五张电影票

2．显示所选电影票的单价和总价

3．可选的电影票、选中的电影票、售过的电影票要有图形颜色或样式区别

4．要能使用图形方式进行电影座位选择

![输入图片说明](https://images.gitee.com/uploads/images/2021/1007/143449_840e1ed7_5122602.jpeg "clip_image002.jpg")

​																						图1－1 

### 三、撰写大作业报告要求

1. #### 说明页面总布局思想及相关实现代码

##### 页面效果截图

![输入图片说明](https://images.gitee.com/uploads/images/2021/1007/143604_bdb23b33_5122602.jpeg "clip_image004.jpg")

 

##### 页面布局思想：

利用一个大的div包括整个页面，然后从中间分开，左边一个div和右边一个div,设置宽度，高度可以不设置，然后利用浮动，就可以实现页面布局，当然如果没有设置给父盒子设置高度的话，需要清除浮动，本次使用的clearfix类名，编写css样式清除浮动，左边盒子可以分成三个部分，头部、中间（使用表格）、底部；右边，分成两个部分，第一部分要继续细分，成左右两部分，然后要再次利用浮动完成布局，第二部分用div向下排列就可以了。

 

##### 相关实现代码：

![输入图片说明](https://images.gitee.com/uploads/images/2021/1007/143622_395a55a7_5122602.jpeg "clip_image006.jpg")

 

2. #### 座位显示的三种状态CSS代码的实现。

![输入图片说明](https://images.gitee.com/uploads/images/2021/1007/143645_5c19fab7_5122602.jpeg "clip_image008.jpg")

![输入图片说明](https://images.gitee.com/uploads/images/2021/1007/143659_0ceab633_5122602.png "clip_image009.png")

给不同的状态设置不同的类名：已选：p0;可选p30;已售：p60

 

3. #### 说明座位实现的原理及相关代码。

相关代码：

![输入图片说明](https://images.gitee.com/uploads/images/2021/1007/143715_f368c337_5122602.jpeg "clip_image011.jpg")

 
![输入图片说明](https://images.gitee.com/uploads/images/2021/1007/143731_325ad4bf_5122602.jpeg "clip_image013.jpg")

##### 实现原理：

当我们座位选中时，我们就利用jQuery给当前座位添加选中的类名，当座位又取消选中时，我们就把添加的类名移除掉。

 

4. #### 说明座位选中的原理及相关实现代码，并对代码附简要说明。（就是用户单位可选座位，在右边相相应位置出现“几行几列”）

![输入图片说明](https://images.gitee.com/uploads/images/2021/1007/143802_fa21a30a_5122602.jpeg "clip_image015.jpg")

![输入图片说明](https://images.gitee.com/uploads/images/2021/1007/143825_44c3ef19_5122602.jpeg "clip_image017.jpg")

##### 代码说明：

首先要获取左边座位的索引，然后对应索引进行判断，已得到行和列，利用jQuery动态的创建一个座位，把行和列加到座位里面去，然后把创建的座位动态的显示到页面上。

 

5. ##### 列出总价的实现代码及代码的简要说明。

![输入图片说明](https://images.gitee.com/uploads/images/2021/1007/143841_ed804b99_5122602.jpeg "clip_image019.jpg")

 

![输入图片说明](https://images.gitee.com/uploads/images/2021/1007/143853_c0849f37_5122602.jpeg "clip_image021.jpg")

##### 代码说明：

定义count为已选座位的个数，countPrice为总价钱，利用公式：总价钱=单价*已选座位的个数，算出总价的金额。
