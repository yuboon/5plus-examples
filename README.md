# 5plus-examples
案例基于5+App实现，uni-app可参考代码和思路进行转换实现，下载后导入Hbuilder运行，因为使用了plus接口，必须真机运行才能看到效果。

## 案例分享

名称 | 路径
------------ | -------------
六位密码输入框 | html/password
数据选择器 | html/pop-picker
时间选择器 | html/dt-picker
Toast提示 | html/toast
输入框输入值限制 | html/input-reg
底部原生TAB&数字角标 | html/tab-native-badge
IOS输入框点击输入延迟问题解决 | html/ios-input
国际化-Jquery实现 | html/i18n-jquery
国际化-Vue实现 | html/i18n-vue
iframe中访问plus接口 | html/iframe

## 问题汇总
#### ◆ 关于原生绘制图标无法显示的问题

> 可能的原因一：原生绘制时，同一个视图中不能引入多个字体库，会出现图标显示错误或显示不出来的问题

_解决办法：使用统一的字体库，避免使用多个字体库_

#### ◆ 关于IOS下调用`plus.zip.compress`无法生成压缩文件的问题

> 可能的原因一：压缩保存的路径问题

_解决办法：保存路径必须带file://同时相对路径为_doc/photo.jpg 或 _www/photo.jpg ，完整路基示例：var distPath = 'file://' + plus.io.convertLocalFileSystemURL('_doc/photo.jpg')



## 小技巧
#### ◆ iframe子页面中调用plus接口

> 存在iframe的页面，调用plus接口，可通过parent.plus调用，详见案例分享中`iframe中访问plus接口`
