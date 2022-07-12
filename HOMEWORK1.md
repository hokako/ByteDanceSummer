## 一、按顺序打印出App、ViewController生命周期的各个事件。

#### App：

点击程序图标

执行main函数

通过UIApplicationMain函数

初始化UIApplication对象并且为它设置代理对象：

- 程序载入后：applicationDidFinishLaunching


- 将要进入非活动状态：applicationWillResignActive


- 程序进入活动状态：applicationDidBecomeActive


- 程序进入后台：applicationDidEnterBackground


- 程序从后台将要重新进入前台：applicationWillEnterForeground


- 内存警告，程序将要终止：applicationDidReceivememoryWarning


- 程序将要退出结束：applicationWillTerminate

  UIApplication对象监听系统事件

  程序结束退出

#### ViewController：

alloc/init：创建对象，分配空间

loadView：初始化对象，初始化数据

viewDidLoad：载入完成，可以进行自定义数据以及动态创建其他控件

viewWillAppear：视图将出现在屏幕之前

viewDidAppear：视图已在屏幕上渲染完成

viewWillDisappear：视图将被从屏幕上移除

viewDidDisappear：视图已经被从屏幕上移除

dealloc：视图被销毁，此处需要对在init和viewDidLoad中创建的对象进行释放

## 二、写出五种常用的 UI 控件

UIScrollView：可显示超过屏幕大小的UI控件，允许滚动和缩放其包含的视图。

UITableView：使用单列来展示数据的视图，只支持纵向滑动。

UICollectionView：一个管理数据项的有序集合并使用可定制的布局来展示它们的对象，支持横向、纵向滑动。

UIWebView：一个显示网页的UI控件，可用来显示pdf、word等文件。

WKWebView

## 三、列举出三个UITableViewDelegate声明的方法

```
1. (void)tableView:(UITableView *)tableView didSelectRowAtIndexPath:(NSIndexPath *)indexPath 
2. (CGFloat)tableView:(UITableView *)tableView heightForRowAtIndexPath:(NSIndexPath *)indexPath
3. (CGFloat)tableView:(UITableView *)tableView heightForHeaderInSection:(NSInteger)section
```

