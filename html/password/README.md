# 6位密码输入框

## 效果图
<p align="center">
	<img src="https://github.com/yuboon/5plus-examples/blob/master/assets/password.png" width="300" height="500">
	<p align="center">
		<em>6位密码输入框</em>
	</p>
</p>

## 实现思路
第一步：使用一个隐藏的输入框，6个密码输入框，采用布局控制让隐藏的输入框覆盖在密码输入框之上。 

第二步：设置隐藏输入框的宽度，超过布局范围，设置文本框内容居右显示，即可实现将光标隐藏。  

第三步：监控输入框的input事件，输入值时触发，将隐藏输入框的值遍历后分别放入密码框。  

第四步：输入完成后，发送事件，打开输入窗口的界面监听输入完成事件，取到输入值完成后续业务逻辑。  

## 其他说明
密码框弹出使用了webview，考虑到样式冲突和兼容性，同时为了保证组件的高度复用（多个页面调用时重复的代码拷贝或类库引入），并未使用div方式，考虑到重复创建webview带来的性能问题，webview仅初次调用时创建一次，关闭时仅对webview做隐藏操作，不真正关闭，随后调用直接显示webview即可。详见代码实现。

