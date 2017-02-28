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