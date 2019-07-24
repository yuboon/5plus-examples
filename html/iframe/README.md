# iframe中访问plus接口

## 效果图
无

## 说明
项目中存在使用iframe的情况时，初次加载可正常使用plus接口，如果界面打开后存在动态加载iframe的情况，则再次调用plus接口会出现plus未定义的情况。

解决办法调用 `parent.plus` 使用iframe父窗口的plus对象调用即可，兼容初次加载及动态加载的情况。