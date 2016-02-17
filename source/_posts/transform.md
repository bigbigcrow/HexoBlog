---
title: CSS3 Transform 3D
date: 2016-02-03 10:13:59
tags:
- CSS3
- Transform
- 3D
---

![Transform 3D 兼容性](/images/3d_compatibility.jpg)

#### 本节将学到Transform的以下知识点：
- rotateX()
- rotateY()
- rotateZ()
- perspective
- perspective-origin
- translateZ
- transform-origin
- transform-style
- backface-visibility


一、** rotateX(angle) ** ：沿X轴（axis）旋转

> 例：`.test{transform: rotateX(45deg);}`

二、** rotateY(angle) ** ：沿Y轴（axis）旋转
> 例：`.test{transform: rotateY(45deg);}`

三、** rotateZ(angle) ** ：沿Z轴（axis）旋转
> 例：`.test{transform: rotateZ(45deg);}`

四、** perspective: number|none ** ：透视、视角

五、** perspective-origin: x-axis y-axis **

六、** translateZ **

七、** transform-origin **

八、** transform-style: flat（平面的）|preserve-3d **

九、** backface-visibility **

#### 综合实例：旋转木马