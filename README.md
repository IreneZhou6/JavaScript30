JavaScript30
Day1--Drum Kit

效果：当键盘上的特定键被按下时，屏幕上对应按钮会产生被点击效果，并且播放对应的音效。 主要技术：使用标签，自定义属性data-xx。

要点： 
JS部分：

    不用监听每个key，只需要在window监听，定义每次键盘按下的那个特定的key；
    transitionend事件可以用于在CSS过渡完成后去除原本的效果，用setTimeOut也可以做到；
    当我们给元素动态加上.playing类的时候，同时加了好几个过渡效果，所以去除效果的时候如果不加鉴别，函数会被调用多次；
    key.classList.add('playing'); key.classList.remove('playing');
    querySelectorAll获得的是一个NodeList，不是array，它没有map，只有forEach；

CSS部分：

    直接给外层父盒子div.keys设置宽高100%无效，因为div作为块级元素本来就是宽100%，其高度如果不设置就会被内容撑开； 或者直接给html设置背景图。
    background-size: cover/contain; 保持图像比例，缩放成将完全覆盖背景定位区域的最小大小/最大大小。
    flex：flex-grow | flex-shrink | flex-basis; 分配剩余空间的相对比例 | 收缩规则 | 在主轴方向上的初始大小。
    rem是相对于html元素的尺寸，因此可以设置其大小为10px，方便后续计算尺寸。

Day2--