# ZWTopSelectVcView
##快速导入多个控制器，通过顶部选择菜单切换控制器，实现一个页面多个控制器切换处理
# How to use：
## Import the header file（设置头文件）
    #import "ZWTopSelectButton.h"
    #import "ZWTopSelectVcView.h"
### 1.To initialize the ZWTopSelectVcView (初始化)
    ZWTopSelectVcView *topSelectVcView=[[ZWTopSelectVcView alloc]init];
    topSelectVcView.frame=self.view.frame;
    [self.view addSubview:topSelectVcView];
    self.topSelectVcView=topSelectVcView;
### 2.Set the delegate of ZWTopSelectVcView（设置代理）
    self.topSelectVcView.delegate=self;
### 3.Start drawing the UI （开始绘制UI）
    [self.topSelectVcView setupZWTopSelectVcViewUI];
##To implement proxy（Have to do）（一步导入你的各种控制器）
   -(NSMutableArray *)totalControllerInZWTopSelectVcView:(ZWTopSelectVcView *)topSelectVcView
   {
   
    NSMutableArray *controllerMutableArr=[NSMutableArray array];
    
    [controllerMutableArr addObject:[[OneTableViewController alloc]init]];
    [controllerMutableArr addObject:[[TwoViewController alloc]init]];
    [controllerMutableArr addObject:[[ThreeTableViewController alloc]init]];
    [controllerMutableArr addObject:[[FourViewController alloc]init]];
    
    return controllerMutableArr;
   }
####Show What it is    
![image](https://github.com/liunianhuaguoyanxi/ZWTopSelectVcView/raw/master/演示/push.gif)
####Show custom size 
![image](https://github.com/liunianhuaguoyanxi/ZWTopSelectVcView/raw/master/演示/自定义尺寸.gif)
####Show one controller can have multiple ZWTopSelectVcView
![image](https://github.com/liunianhuaguoyanxi/ZWTopSelectVcView/raw/master/演示/多个view.gif)
####Show some of the effects 

![image](https://github.com/liunianhuaguoyanxi/ZWTopSelectVcView/raw/master/演示/水波.gif)![image](https://github.com/liunianhuaguoyanxi/ZWTopSelectVcView/raw/master/演示/淡入淡出.gif)![image](https://github.com/liunianhuaguoyanxi/ZWTopSelectVcView/raw/master/演示/翻转.gif)![image](https://github.com/liunianhuaguoyanxi/ZWTopSelectVcView/raw/master/演示/覆盖.gif)![image](https://github.com/liunianhuaguoyanxi/ZWTopSelectVcView/raw/master/演示/翻页.gif)

####具体设置详情在demo中
####如果你有任何疑问，欢迎随时发邮件到menglanfenghen@163.com
