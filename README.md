# 5plus-examples
案例基于5+App实现，uni-app可参考代码和思路进行转换实现，下载后导入Hbuilder运行，因为使用了plus接口，必须真机运行才能看到效果。

## 案例分享

名称 | 路径
------------ | -------------
六位密码输入框 | html/password
数据选择器 | html/pop-picker
时间选择器 | html/dt-picker
Toast提示（美化） | html/toast
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

_解决办法：保存路径必须带file://同时相对路径为_doc/photo.jpg 或 \_www/photo.jpg_

_完整路径获取示例：`var distPath = 'file://' + plus.io.convertLocalFileSystemURL('_doc/photo.jpg')`，兼容IOS与Android_

#### ◆ 5+项目打开新窗口后，点击返回按钮提示退出应用

> 可能的原因一：未引入官方的common.js

_解决办法：使用hbuilder建立Hello 5+ 样例工程，从中拷贝common.js到项目中，在新窗口页面引入该common.js_

#### ◆ mui prompt 使用div方式时，出现页面滚动的情况

> 可能的原因一：界面样式冲突或不兼容

_解决办法：可将prompt显示出来的div内容块复制出来（使用官方mui在线演示通过浏览器调试工具选择复制），放在当前页面，自主控制div的隐藏显示即可_


## 小技巧
#### ◆ iframe子页面中调用plus接口

> 存在iframe的页面，调用plus接口，可通过parent.plus调用，详见案例分享中`iframe中访问plus接口`

#### ◆ plus接口调用问题

> IOS上mui.ready函数中可以正常调用plus接口，Android则不行，建议强制全部使用plusReady

#### ◆ 新打开界面向打开它的界面传值

> 方式一：新打开界面调用`mui.fire()`函数, 打开界面调用`window.addEventListener`监听

> 方式二：新打开界面调用`var opener = plus.webview.currentWebview().opener()`获取打开它的窗口对象，调用`opener.evalJS('alert(1)')`注意evalJS中的函数或变量需为全局变量

