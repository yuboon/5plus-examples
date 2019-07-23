# 时间选择器

## 效果图
<p align="center">
	<img src="https://github.com/yuboon/5plus-examples/blob/master/assets/dt-picker.png" width="300" height="500">
	<p align="center">
		<em>时间选择器</em>
	</p>
</p>


## 说明
官方的picker使用div方式，使用过程可能出现当picker层被覆盖无法显示、页面存在滚动条时可能导致的picker显示不全的问题.

dt-picker弹出使用webview进行包装，可有效解决上述的两类问题，同时保证了组件的高度复用（多个页面调用时重复的代码拷贝或类库引入），考虑到重复创建webview带来的性能问题，webview仅初次调用时创建一次，关闭时仅对webview做隐藏操作，不真正关闭，随后调用直接显示webview即可。详见代码实现。

