##transform(2d变换)
###旋转
	transform:rotate(360deg);
	rotate中的参数以deg为单位;
		
		正值:顺时针旋转
		负值:逆时针旋转
	
	只能设单值。正数表示顺时针旋转，负数表示逆时针旋转
###斜切
	transform:skewX(45deg);
	skewX(45deg):参数值以deg为单位 代表与y轴之间的角度
	skewY(45deg):参数值以deg为单位 代表与x轴之间的角度
	skew(45deg,15deg):参数值以deg为单位 第一个参数代表与y轴之间的角度
									第二个参数代表与x轴之间的角度
									
		正值:正斜杠方向
		负值:反斜杠方向
	
	单值时表示只X轴扭曲，Y轴不变，如transform: skew(30deg);等价于transform: skew(30deg, 0);
	考虑到可读性，不推荐用单值，应该用transform: skewX(30deg);。skewY表示只Y轴扭曲，X轴不变
###缩放
	transform:scale(2);
		
	同样可以设单值和双值。单值时表示X轴和Y轴等值缩放。默认值为1，要缩小请设0.01～0.99之间的值，
	要放大请设超过1的值。
	例如缩小一倍可以transform: scale(.5);
	放大一倍可以transform: scale(2);
	
	如果只想X轴缩放，可以用scaleX(.5)相当于scale(.5, 1)。
	同理只想Y轴缩放，可以用scaleY(.5)相当于scale(1, .5)
	
	w3cschool上没说的是，scale还能设负数，负数会先将元素反转再缩放，
	如transform: scale(-.5, -1.5);
	为何反转能理解吧？XY轴像素矩阵各值取反后，效果等价于反转。当然你同样可以用rotate实现反转。
###位移
	transform:translate(-100px,200px);
	translateX(100px)
	translateY(200px)
	
		正值:往左/往下
		负值:往右/往上
		
	可设单值，也可设双值。正数表示XY轴正向位移，负数为反向位移。设单值表示只X轴位移，Y轴坐标不变，
	例如transform: translate(100px);等价于transform: translate(100px,0);
###变换基点
	transform-origin:right bottom;
	transform-origin:200px 200px;(参照左上角,0 0就是左上角)
	
	rotate:中心点
	skew:中心点
	scale:中心点
	translate:本身
