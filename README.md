### 时间插件	
 当js文件直接引入到和HTML中。可以在vue的方法里面混用此插件。直接初始化,在文件初始化之前请引用jquery。 
 初始化的方法。 
 ```
<input type="text" id="dt" placeholder="trigger calendar"> 
<div id="dd"></div>
//在script中初始化
 $('#dd').calendar({
	trigger: '#dt',
	zIndex: 999,
		data:[ {date: '2017/3/3', value: '面试'},{date: '2017/3/5', value: '面试'} ],
		format: 'yyyy-mm-dd',
	onSelected: function (view, date, data) {
	    console.log('event: onSelected')
			console.log('date:' + date)
	},
	onClose: function (view, date, data) {
	    console.log('event: onClose')
	    console.log('view:' + view)
	    console.log('date:' + date)
	    console.log('data:' + (data || 'None'));
	}
    });
 ```