转自[《UE4从菜鸟到高手合集版》笔记](https://www.yuque.com/docs/share/1daa39ff-a55d-44c2-98c1-69c783689ea2)，有修改



# 04 基本操作和常用快捷键

鼠标左键或右键 + Z/C          



鼠标左键 + Alt + 拖拽          围绕一个单独的支点或兴趣点翻转视口

鼠标右键 + Alt + 拖拽          向前推动相机使其接近或远离一个单独支点或兴趣点

鼠标中键 + Alt + 拖拽          根据鼠标移动的方向将相机向左右上下移动



Alt + G/H/J/K          在不同的视图中切换

# 05 播放模式

Shift + F1          在运行时将鼠标移出

### 在运行中修改

按F8：在运行中修改。（一边运行游戏一边修改游戏中的物体）

但不会保存！

想要保存，选中，右键

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1615949451983-1b86594f-1f15-4572-9cf2-9c2483d589fd.png)



![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1615949971820-9fc489f8-fd22-4157-809d-1c0ac044b243.png)

上面这张图是添加一个球，模拟物理

Play里有个Simulate，可以理解成F8的高级版。

Play之后暂停，有Frame Skip，每按一次将使游戏快进1帧

# 06 搭建一个小屋

# ![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1615950333832-defe9635-39ad-41bb-9728-e089a15a4b6a.png)

## 新建level



![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1615950517291-031bb164-8ca8-4abd-832c-b5f06eb4d0a5.png)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1615950555847-5d04d33f-5838-4e35-9375-083b6d751c60.png)

新建的Level在“项目名CPP”->Maps文件夹里

## 观察某一物体

alt+鼠标左键

shift+移动某一个轴：摄像机也跟着动啊

## 放椅子

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1615951183721-68c7e59e-0081-4d46-b250-b958f93b8fb5.png)

## 聚焦

f

## 等比缩放

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1615951300332-fa7f6751-a7a3-44fa-ac25-777b5d72e1a7.png)

## 吸附到地面

End键！

## 打组

Ctrl+g

shift+g脱离打组

spotlight 聚光灯

# 07 Geometry搭建场景

对Geometry里的Box，面、点编辑

Mode下拉，Brush Editing，可以拖拽某个面，某个边，某个顶点



## 做门

有先后顺序，先放墙，后放门，才可以相减掉

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1615955659319-2dd3e9a4-c675-45fd-9c76-6cf1e6e72cd2.png)

# 08 材质操作

## 选中玻璃

按t选不中，再按t选中玻璃啊，这是对于半透明物体的快捷键

## 选择墙面

## ![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1615957270663-7be81b3f-6e37-4160-9671-618421eb5ff5.png)

这是在Detial->Geometry里面，还有其它的选择方式

## 移动材质

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1615957475479-d6aee32e-e1e6-445e-a5fd-edf94bbdd939.png)

Alignment可以材质调整对齐

Pan，Rotate，Flip是移动旋转翻转材质

# 09 关于蓝图简介

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1615958025396-251ac3f8-cbc5-4cab-b232-5503cab3e1c4.png)   

一个关卡只有一个蓝图

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1615958126524-a222c99c-dcfd-435a-b517-f63a448630b1.png)

蓝图中的变量要按住Ctrl拖进Event Graph

蓝图按右键弹出上下文，有很多类型

# 10 Event事件节点

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1615959110149-0270daff-81da-4aeb-b4d0-57b9584a894d.png)

Event时间节点在单一蓝图中每种类型只能使用一个

## EventBeginPlay节点

游戏开始在所有Actor上触发此事件

## 给灯光创建引用（变量的别名）

选中灯光

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1615959296565-33d2689a-a832-4164-9c07-1a61a9b25ee6.png)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1615959310230-78427258-d3e5-4bd1-8946-51ec163837fa.png)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1615959431856-8b66f079-0278-411f-9aa9-e0868ec72900.png)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1615960568781-ee691254-e8b0-4892-ae58-f648f2433024.png)

这里的Toggle Visibility是从PointLight拖出来才有的，切换可见性

 

## 使灯不亮

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1615960728364-729ba752-6fd5-46c0-a5df-53d504e28fea.png)

visibility是可见度的意思。

白色的那个引脚叫执行引脚ExecutionPin，创建了一个执行流。

# 11 重叠事件讲解

## OnActorBeginOverlap和OnActorEndOverlap

重叠是碰撞的一部分

## 进入灯的范围，灯亮，离开，灯灭

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1615961190974-29f4600b-36d6-475e-a5dc-366df86ab195.png)

在灯的范围加一个盒体触发器

然后在Viewport选中它，再去蓝图中添加碰撞里的触发事件

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1615961326090-ab6c342d-f3c9-4bff-a044-4614bad29d5f.png)



一个函数可以由多个事件触发

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1615961776728-965d27a1-e8b8-4eb3-bad3-c5d3aca1164f.png)

## 延迟几秒

按Alt + 鼠标左键就可以删除连线

## 

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1615961913341-4c51f8db-49be-4d54-aca2-81524c908e0d.png)

# 13 碰撞概述（上）

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616041732861-06d5267b-7c53-4419-ad90-6743c31f283c.png)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616042182964-778e0841-8e5b-4fbf-8af2-7b95be4d7389.png)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616042543486-601633b9-301b-4427-b93d-d16c90c2b051.png)

## 添加碰撞事件——block

产生碰撞的效果，但是没通知（函数），如果要产生通知，要勾选模拟生成碰撞事件

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616043132490-30c0e0bf-a325-4ec2-9fdc-88194696c840.png)

选中此物体，然后打开level blueprint

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616043310878-98a1137f-3362-4286-b166-9cf9c4218b3b.png)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616043342814-27fc9e88-510d-454a-b1f2-5bf9b9be827d.png)

添加完成

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616043363023-e4abc37b-08da-4b83-84dd-0a5c6957c1be.png)

## 打印碰撞物体的名字

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616043548803-b4ec9912-e76c-41a4-8cb7-9a6b25c79f80.png)

这里的Print String是自己右键找到的，中键的Get Display Name是连接Other Actor和In String自动生成的

# 14 碰撞概述（下）

如果两物体发生重叠，那么双方都要勾选Genetate Overlap Events：

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616044252900-583887ff-7b97-418e-90bc-9259df432b9a.png)

## 添加overlap

overlap和block和区别，进入和退出的适合会有通知！

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616045579140-a9887613-7338-490b-8bff-e7cd65cd96f4.png)

要看对象的Object Type

然后在请求重叠的主体中设置：

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616045755354-fe4f5151-4e5c-4862-835c-786dcb1faa27.png)

也就是此物体，只和vehicle产生重叠效果。

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616046042104-d95727e2-9b17-40c8-9eb4-1a706fc4e040.png)

# 15 作业讲解

ignore：直接穿过去，不产生事件

overlap：穿过去和出去发生通知，双方物体必须勾选 Generated Overlap Events

block：不会物体中穿过去



主角没勾选Generate Overlap Events，但还是能碰撞，因为它的CapsuleComponent勾选了

# 16 类蓝图简介

其实应该叫蓝图类

Content Browser右键创建Blueprint Class，选择父类，然后可以Add Component，还可以点进去修改。

然后就可以拖出来实例化

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616119922461-71acd3ed-72f2-4ab0-9013-4ec0bfb6ed59.png)

蓝图类有三个面板，Event Graph和关卡的是一样的，Construction Script可以理解成蓝图类的构造函数，Viewport就是看它实例化的地方



根据代码创建蓝图

## 改变控制的对象

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616148731130-f050c0bf-0e0d-41b3-b9d9-272d0e456831.png)

这里是在项目设置里Maps & Modes改Default Modes，主角也会变成一个球

## 蓝图基本操作

快捷键

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616149085830-511edf78-d310-4540-857b-a6ca9a8b5258.png)

# 17 类蓝图实现灯光开关效果

## 关闭自动保存

# ![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616149370778-99400376-b9b0-4aff-a197-57d3249e1163.png)



创建蓝图类，Add Component添加一个点光源，再从初学者内容里拖过来一个灯罩，再Add Component添加一个Box Collision。注意他们的层级关系要弄成并列的。

在这个蓝图类的Event Graph里，可以像之前关卡的那样，选中Box右键加碰撞On Component Begin Overlap（关卡里是用的 On Actor ...），Point Light拖出Toggle Visibility(这两个之前比关卡蓝图的少了个东西，因为是在同一个类里面)。

# 18 作业讲解

## 父子关系

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616206831169-9a2a326e-062e-44ea-86aa-c459faddb1d7.png)

不能缩放Box

所有能拖到场景中的都叫Actor！

## On Component End Overlap（Box)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616209740169-f9a863cd-84e5-483a-a5d4-cca4a8415cf2.png)

离开cube后消失

# 19 按键响应

## 如何使用中文字体

### 3D UMG

https://www.bilibili.com/video/BV1xa411w7bi?from=search&seid=10280643562821518528



## 设置刚开始是否显示？

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616213563854-ea3b70da-58d4-458e-b32a-e56326344fb0.png)

这节的蓝图类是：靠近会显示提示信息让按F，按下后灯会亮，离开时提示信息小时，按F没反应

tips是Add Component找到Text Tender，Enable/Disable Input需要Player Controller，我们就用Get Player Controller。按F控制灯的开关，如果Disable Input了按F是没反应的，只有和Box重叠的时候Enable Input按F才有用。（上面图的cube Destroy不是这节的）

# 20 作业讲解

## 物体隐藏

设置物体隐藏是Set Actor Hidden In Game，New Hidden指的是是否隐藏此actor和它的所有component

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616297672872-6577a1aa-091e-4d5b-911b-13b678377d8a.png)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616297708249-e4bc0ee0-17b5-451d-98f4-34a413a84eea.png)

## 设置碰撞通道

按下之后就可以穿过去

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616298030085-e0224928-626f-42bf-99d0-f96c27354045.png)

## 物体所有有关事件

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616300029452-cba658aa-eae5-4a1d-a91d-1d7dd2edfe8e.png)

## 加注释

框选+快捷键C

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616302452314-0722e679-d683-4259-8ab9-69ffd882e653.png)

# 21 变量的概念

## 转换为类蓝图的两种方法

### 1、

​         ![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616304418514-25c11ec6-7312-4696-b632-b562eb034652.png)

### 2、![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616304468274-160e9aa7-a9c3-400f-a9ac-f30863dafff5.png)



UE4中的变量类型

String，Text，Name的区别

String字符串类型

Text代表显示的文本数据，尤其是在文本需要本地化的地方

Name用来存储名字的变量，例如类名，名字也是一串文本，只是它可以用来识别游戏中的一些元素



## 变量是否可编辑

点亮这个小眼睛，就可以在主编辑器编辑。它其实是Details里的Instance Editable。

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616304611299-9a398f11-3c58-4060-9b6b-656f769c19cd.png)



Tooltip是鼠标移到变量上会显示的提示。

Expose On Spawn是它在类蓝图是否作为一个引脚

Private是让不让子类访问

Category是把它放到一个类别里



![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616304624165-c1215526-698e-414d-846c-116cceb31457.png)

# 22.Unreal Engine使用蓝图制作FPS游戏01

实现发射子弹打到的Cube变红

新建材质球

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616334766359-10432b0d-a8c7-487e-bb8f-a1682c133cf0.png)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616334779890-ad6f79f9-4852-4ba9-aaee-39de207b1145.png)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616335874076-16efe876-9f1b-4e91-89e6-e4d9b890b3c8.png)

VectorParameter是Vector类型的变量，存储的是颜色信息，RGBA

按1，单击，出现一维向量，同理，二三·····维

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616336092313-bec58d0e-cf82-4f6b-b628-e695d8925e6a.png)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616337084182-6e11d8cd-628d-47de-b9b4-f1dcb89fa3c6.png)

## 选中Cube转化为类蓝图

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616337258565-9d0a6bf3-0842-4f56-8314-d488a9e196dc.png)

## Event Hit击打效果（上材质）

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616338218452-769699e9-6607-464e-9997-85fa8d1e69cc.png)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616338448966-e3de11c3-1d18-4424-9c67-7af2e55528bd.png)

## cast to FirstPersonProjectile

> FirstPersonProjectile 为模型球

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616374872056-71bf4c79-7563-4649-8630-f9edf3b6449c.png)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616374743149-b27d3ee6-41c0-4e88-8664-c316a48b4c1e.png)

Other代表命中的其他Actor

使用cast to xxx节点可以检查是否为命中的其他Actor

cast是C++中父类转化为子类的一种语法方式

# 23.Unreal Engine使用蓝图制作FPS游戏02

## 添加变量

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616375717879-71a07670-4a6e-4f14-a6a6-3ce21570962c.png)

Speed-float

Direction-vector

## 不同帧速率下，效果相同（标准化）

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616375856799-d317ee01-110b-48b9-8a3d-c55a01d1e61c.png)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616375883192-c890d2e3-cce8-4b6d-bcea-1d2f2f5d9600.png)使得不同帧速率下，效果相同

## 向量标准化

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616376084411-b365c8a5-457a-4418-968b-ca3eea2114d8.png)

标准化速度

## 获取物体变换数组并分割出坐标再并移动

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616379732649-5d4b4cee-7092-495e-b694-5f65f0d9c2c3.png)

## 来回移动，FlipFlop反转

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616380897844-e06f5e40-d578-4f85-a9b0-5648975d2ce5.png)

第一次调用输出A，第二次调用输出B

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616381232540-64755f56-aee9-4fa9-9bd6-2f64b9fdb438.png)

# 24.DeltaTime的作用

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616381475204-6ec47d52-f052-4198-a509-f8bb090e54d2.png)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616381609092-fc1829eb-211c-4e9b-8cc4-000d8bd83d58.png)

## 显示/更改FPS

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616381826370-ed8a6b4c-843a-4663-8356-3b85f8c44a33.png)

更改fps

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616381925442-3beac3c8-94e6-468f-b603-210a80e764eb.png)

# 25.作业讲解

## 第一题

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616386532636-c1c59a02-a22f-470e-9532-396d6b17e1d9.png)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616386553421-ea88eab8-9494-4a8c-88d4-e9cb722d3f72.png)

## 第二题

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616386648354-5a89d992-c7d1-43b2-af83-6e76993b673b.png)

**两class类直接如何发生交互？**

### 1、在Level Blueprints实现

添加Ondestory

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616387431566-f52ff0ab-f277-4777-a6b9-05e9ef71483e.png)

### 2、类内实现（发通知）

## 第三题

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616387883098-a9de1902-0e1b-4b90-b9db-e93b19345078.png)

# 26 实现人物加速

## 添加按键

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616411628428-a3505a48-df90-4c83-a694-3d19a4d48e7a.png)

## 加速操作

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616412375540-abf8d3da-b794-4fa3-8e31-c7d9fca27d2c.png)



# 27 实现开镜操作

## 单纯放大

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616412810681-2567ae4e-8ca8-4fd3-8cc2-5a718330b5fd.png)

## Timeline

淡入淡出，开门关门，补间动画吧

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616413432989-ffe42f19-01ff-4176-9a19-6715b5c86656.png)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616413753426-fd242eda-8d3c-48f3-a7a9-1ead7e4d756a.png)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616413766927-fbd1d828-63be-4b79-a577-6befc33c50a8.png)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616413809218-a9fbc014-6c9b-424d-a8f1-575af7259b75.png)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616414578229-37d96e6c-0c68-40c9-a919-27d9ebcc0381.png)

reverse反向播动画

# 28 Timeline节点讲解

基于时间的动画

淡入淡出的效果，线性动画

虚幻引擎4有一个被称为“Tick”的事件，它产生于游戏的每一帧。例如，在一个运行在每秒60帧的游戏中，“Tick”事件会在每一秒产生60次。

“Tick”事件提供了一个被称为“delta秒”的值，该值是自上一帧结束后的时间。使用事件“Tick”，我们可以精确控制在游戏中的蓝图的运动。

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616722130722-c8ad864b-6bd9-4f29-b43f-6e93d2646e7c.png)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616721642296-b0f04c2f-f103-4f36-86e5-bac85af0ce51.png)

# 29 TimeLine开门案例

和上一讲差不多，不再赘述

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616723153892-69dc6337-6d71-4c57-9f5d-cade69a9bbc0.png)

# 29 增加子弹速度

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616723722104-a42b95d2-55c9-4d01-bbd6-0504a7ed74a9.png)

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616724264848-e9e6bb67-607c-44bd-8d82-aac2982af8a8.png)

# 30 当物体销毁时播放声音

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616724551635-168a2fc1-3750-401a-a3c3-bcdd71332384.png)

# 31 添加爆炸效果

![image.png](https://cdn.nlark.com/yuque/0/2021/png/12595208/1616724749537-671c7f28-e273-4acc-afb7-2cd6039942b9.png)

- [03 面板介绍](#PK9Bl)
- 