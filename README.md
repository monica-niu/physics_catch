# physics_catch
一个基于CreateJS+p2.js的抓娃娃DEMO （移动端适配） 

Please user your mobie to visit this url

## 操作说明

  左右滑动移动爪子，下滑抓娃娃。

## 项目总结

  用了3天研究物理碰撞引擎的使用，刚开始试了cocos2dx-js，接触了chipmunk，但是学习资料太少了，API还得翻chipmunk.js一个一个找，于是放弃了。
  
  cocos2dx-js的学习资料也很少，不得以网上买了一本cocos2dx-js的书，到手以后，兴奋的放开物理引擎那一篇，想摔书，就4页左右，还和网上的chipmunk教学
  一模一样。
  
  后来转用白鹭引擎，总的来说各个引擎的模式都差不多，按白鹭官方的推荐用了p2.js这个物理引擎，因为要导入额外的拓展包，于是去p2.js的官网下载，发现p2.js
  竟然有pixi.js的渲染demo，顺藤摸瓜，终于搞清楚了各大物理引擎的渲染原理，于是改用比较熟悉的CreateJS来完成这个项目。
  
## 映射
  其实物理引擎和其他的动画引擎是分开的，一个负责渲染图形，一个负责创建物理世界，然后将图形绑定到物理世界的物理模型上（坐标，旋转角度等），
  实时更新图形的数据。一般物理世界都是很小的，所以最开始需要定义一个缩放比例，将小的物理世界的数据放大到图形舞台中。
