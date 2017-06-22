## UITableView 相关资料
- 一句代码解决UITableView 中的分割线顶格问题

```objc
self.tableView.separatorInset = UIEdgeInsetsZero;
```

------------------
## cocoapods 创建Podfile
- cd 项目路径/
- touch Podfile
- vim Podfile   

```
inhibit_all_warnings!
platform:ios,'8.0'
use_frameworks!

target "项目名称" do
pod 'MJExtension'
end
```
- esc,:wq 保存退出
- pod install

--------------------
## 使用Xib AutoLayout布局控件设置规定尺寸但显示效果不是自己想要的，加入以下属性

```objc
self.autoresizingMask = UIViewAutoresizingNone;
```

--------------------
## 隐藏Group TableView上边多余的间隔
- 这个间隔其实是一个被 UITableView 默认填充的 HeaderView。而且，视图的高度不能为0，否则完全不起效果。但我们用下面的代码创建一个高度特别小的 HeaderView 时，上面的边距就不见了

```objc
self.tableView.tableHeaderView = [[UIView alloc] initWithFrame:CGRectMake(0, 0, 0, CGFLOAT_MIN)];
```

--------------------
## 跳转到苹果商店下载页面/评论页面
- 跳转到苹果商店下载页面

```objc
NSString *str = [NSString stringWithFormat:@"itms-apps://itunes.apple.com/app/id%d", app_id];
```

```objc
[[UIApplication sharedApplication] openURL:[NSURL URLWithString:str]];
```

- 跳转到苹果商店评论页面

```objc
NSString *str = [NSString stringWithFormat:@"http://itunes.apple.com/WebObjects/MZStore.woa/wa/viewContentsUserReviews?id=%d&pageNumber=0&sortOrdering=2&type=Purple+Software&mt=8",app_id];
```

```objc
[[UIApplication sharedApplication] openURL:[NSURL URLWithString:str]];
```

---------------------
## 在一个自定义的View中,或者自定义cell中,modal出一个控制器建议使用
```objc
[UIApplication sharedApplication].keyWindow.rootViewController;
```

代替

```objc
self.window.rootViewController
```

因为程序可能不止一个window,self.window可能不是主窗口;

---------------------























