# year2016
2016年的技术沉淀

1、关于slider效果显示问题
相关链接点击<a href="http://codepen.io/xianJohn/pen/zoWYZe?editors=1111">好看的slider</a>

2、nginx
nginx代理配置名小写

3、ie10和ie8双击打开file类型的input，设置opacity为0的block，element并设置其字体

4、ie10中不支持vue自带的回车键事件

5、xp只支持到ie8

6、JavaScript易错知识点整理
http://www.jianshu.com/p/1c77853d4f01

7、关于2016年比较火的技术
https://segmentfault.com/a/1190000007805673

8、关于div自适应布局问题

应用的节点
<div class="listItem details-content-item" v-for="item in items" v-bind:class="{'nomr': (($index+1) % pageNumber)==0 && $index>1}" v-bind:style="{marginRight: columnArrow+'px'}">
主要函数
   var boxWidth = $(".list").width()-60;
   var itemWidth = 180;
   this.pageNumber = Math.floor(boxWidth/itemWidth)-1;
  this.columnArrow = (boxWidth-this.pageNumber*itemWidth)/(this.pageNumber-1);
  nomr的让margin-righ为0px。
  
9、时间插件问题

