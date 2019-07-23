# 数据选择器

## 效果图
<p align="center">
	<img src="https://github.com/yuboon/5plus-examples/blob/master/assets/toast-success.png" width="150" height="50">
	<img src="https://github.com/yuboon/5plus-examples/blob/master/assets/toast-error.png" width="150" height="50">
	<p align="center">
		<em>Toast提示</em>
	</p>
</p>


## 说明
官方mui的默认toast或原生toast的均不够漂亮，因此使用toastr.js进行封装。

官网：https://codeseven.github.io/toastr/demo.html

Github: https://github.com/CodeSeven/toastr

toast提示使用webview进行包装，保证了组件的高度复用（多个页面调用时重复的代码拷贝或类库引入），考虑到重复创建webview带来的性能问题，webview仅初次调用时创建一次，关闭时仅对webview做隐藏操作，不真正关闭，随后调用直接显示webview即可。详见代码实现。


