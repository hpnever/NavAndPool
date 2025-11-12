对象池插件：

SimpleObjectPool
核心节点：



<img width="678" height="313" alt="image" src="https://github.com/user-attachments/assets/ff7eda54-8270-4bef-b2e1-4ae318bf643b" />
<img width="787" height="454" alt="image" src="https://github.com/user-attachments/assets/58b1c89c-692a-4fcd-9b84-c7876d82bb27" />



节点解释：

  1.目标（Target）
  
  2.Actor Class（要生成的类）
  
  3.Spawn Location（生成位置）
  
  4.Spawn Rotator（生成旋转）
  
  5.Automatically Return Pool（是否自动回收）
  
  6.Recycling Time（回收时间）
  
  7.Return Value（返回值）返回池里取出来的那个Actor引用


  
<img width="649" height="300" alt="image" src="https://github.com/user-attachments/assets/5930adfb-580b-434e-b43d-9fbb74af12a0" />




3D寻路插件：


SimpleOctaNav3D
核心节点：



<img width="402" height="503" alt="image" src="https://github.com/user-attachments/assets/f763df92-e46f-4abd-8c25-4890c6f5c3ec" />





节点解释：

（用的是胶囊体碰撞检测，胶囊体的半径和半高要配置）

1.目标（Target）

    调用的导航体（Simple Octa Nav Volume 3D）实例
    
2.Start

    起点坐标
    
3.Destination

    终点坐标
    
4.Object Types

    碰撞检测的物体类型   告诉系统哪些物体算“障碍物”（一般默认Actor）
    
5.Actor Class Filter

    可选过滤器
    
6.In Actor

    当前参与寻路的Actor
    
7.Detection Radius

    探测半径     胶囊体的半径
    
8.Detection Half Height

    探测半高     胶囊体的高
    
9.Out Path

    计算出的路径点数组
    
10.Return Value

    返回布尔值，是否找到路径




启用插件后在放置Actor面板那里搜索 SimpleOctaNavVolume3D

<img width="473" height="1032" alt="image" src="https://github.com/user-attachments/assets/eba8d440-5ac8-4298-9618-0d0f23084501" />

第一个就是插件的导航网格了！

在右边SimpleOctaNavVolume3D的细节面板里面根据需要调整一些参数

<img width="520" height="529" alt="image" src="https://github.com/user-attachments/assets/6ce7e21e-eae2-4adb-8225-890c6fea307c" />





1.Pathfinding

  Divisions X / Y / Z
  
     网格划分数量 
     
  Division Size
  
     每个格子的边长
     
  Min Shared Neighbor Axes
  
     最少共享邻轴数  （控制八叉体节点之间的连通规则，默认0即可。调大可减少节点连接，优化性能）
     
2.Aesthetics（外观）

  Line Thickness
  
     网格线条粗细
     
  Color
  
     可视化颜色
     
3.Octree（八叉树结构）（默认就可以了）

  Octree Max Depth
  
    八叉树最大深度  （控制递归细分层数。越大，分辨率越高，但耗性能）
    
  Octree Min Cell Size
  
    最小单元格大小   （限制八叉树最小分割尺寸，防止无限细化）
















    
