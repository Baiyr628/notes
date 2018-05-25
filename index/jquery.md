# jquery复习
### jquery语法

    $(document).ready(function(){ //防止文档在没有加载完之前执行jq
	    $("p").hide(); //隐藏所有p
	    $("#text").hide(); //隐藏id="text"
	    $(".text").hide(); //隐藏class='text'
	    $(this).hide(); //隐藏当前文本
    })
    
### jquery选择器

#### 元素选择器
	例如： $("p")    $("p#text")    $("p.text")
#### 属性选择器
	eg: $("[href='#']")  //选取带有href='#'属性的元素
	    $("[href != '#']")  //选取href 不等于 # 属性的元素
	    $("[href $= '.jpg']")  //选取href 后缀为 jpg 属性的元素
	    $("[href]")
#### css选择器
	eg: $("p").css('background','red')
### jquery 事件函数
#### jquery名称冲突
	var jq = jquery.noConflict() //用jq来代替$
#### jquery事件
	bind();  eg: $('button').bind("click",function(){}) //向button绑定一个click事件
	unbind()   //移除绑定事件
	blur();  eg: $("input").blur(function(){}) //当指定区域是去焦点触发function(){}
	focus();  eg: $('input').focus(function(){} //当指定区域获取焦点执行funcyion(){}
	change(); eg: $('input').change(function(){}) //指定区域发生改变时执行方法，仅适用于select,textarea
	click();  eg: $('p').click(function(){}) //点击事件
	dblclick(); eg: $('p').dblclick(function(){}) //双击事件
	delegate();  eg: $('p').delegate(clickSelecter(必需)，event(必需)，data(可选)，function(必需))  //向匹配元素当前或者未来子元素附加一个或者多个事件事件处理器   
	undelegate();  //移除deleget()添加的一个或者多个事件处理器            
	die();  eg: $("p").die()  //移除所有通过live()方法向p添加的事件
	live(); eg: $('p').live(click,function(){}) //为当前或未来匹配元素添加一个或者多个事件处理
	error(); eg: $('img').error(function(){}) //图片加载失败时，执行function
	event.defaultPrevent()  //阻止事件默认动作
	event.isDefaultPrevented() //返回event对象是否调用了event.defaultPrevent()
	event.pageX()  //相对于文档左边鼠标的位置
	event.pageY() //相对于文档左边缘鼠标的位置
	event.result()  //显示最后一次点击事件的返回结果
	event.target()  //触发该事件的dom元素
	event.type()   //描述事件类型
	event.which()  //显示按得哪个键
	keyDown()  //按下的时候触发事件
	keypress()  //在输入区域按键次数
	keyup()  //按键上来的时候触发事件
	load()  //加载完成触发
	unload()    //当用户离开页面时
	mousedown()   //按下鼠标触发
	mousemove()   //鼠标在移动时触发事件
	mouseleave()    //指针离开元素触发事件
	mouseout()    //指针离开元素或者元素包含的子元素都会触发事件
	mouseover()   //指针进入指定元素或者制定元素包含的子元素触发事件
	mouseenter()   //指针进入元素触发事件
	mouseup()    //松开按钮是触发事件
	one()  eg:$('p').one('click',function(){})   //p只会执行一次click
	ready()   //在文档加载完之后执行
	resize()    //对浏览器窗口大小调整计数
	scroll（）  //对元素滚动进行计数
	select（）   //被选中时触发事件
	submit()    //提交表单时触发事件
	toggle()    //切换
	trigger()   //触发
	triggerHandlar()    //触发被选元素的指定时间，阻止默认事件，不会发生冒泡事件
	