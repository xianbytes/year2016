# year2016
2016年的技术沉淀

1、关于slider效果显示问题
相关链接点击<a href="https://codepen.io/xianJohn/pen/zoWYZe?editors=1111">好看的slider</a>

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
应用的节点关于vue组件的
<code><div class="listItem details-content-item" v-for="item in items" v-bind:class="{'nomr': (($index+1) % pageNumber)==0 && $index>1}" v-bind:style="{marginRight: columnArrow+'px'}"></div>
</code>
主要函数
 <code> var boxWidth = $(".list").width()-60;
   var itemWidth = 180;
   this.pageNumber = Math.floor(boxWidth/itemWidth)-1;
  this.columnArrow = (boxWidth-this.pageNumber*itemWidth)/(this.pageNumber-1);
  nomr的让margin-righ为0px。</code>
9、时间插件问题
10、<a href="https://www.jb51.net/article/28054.htm">deferred解决非同步问题</a>

11.<a href="https://github.com/jsfront/month/blob/master/2016/201612.md">前端分享周报</a>

12、vue计算属性的重要性
data: function() {
        return {
            isCanShow: true,
            collectionBox: false,
            resourceCollectFlag: false,
            image: this.response?this.response.thumbnailsImg:"",
            imageList: this.response?this.response.imageList:[],
            count: -1
        }
    },
    computed:{
        imageUrl:function()
        {
            debugger
            return this.response.thumbnailsImg+"ddd";
        }
    },
    解决了filter不能解决的问题</br><br>
    
13、vue2.0和1.0的区别
   <a href="http://www.imooc.com/article/14438">vue2.0和1.0的区别</a>
   a.目前的项目几乎每个页面都用到了1.0的ready钩子函数，然而2.0已废弃不用，进而使用mounted替换，同时还新增了beforeMount、beforeUpdate、updated等，私以为越来越向react看齐了有木有。。

beforeUpdate的作用是在页面初始渲染视图之后，一旦监测到data发生变化，在变化的数据重新渲染视图之前会触发beforeUpdated钩子函数，这也是重新渲染之前最后修改数据的机会

update的作用则是在data发生变化渲染更新视图之后触发。

b.同时废弃的还有events、$dispatch、$broadcast，官方推荐使用vuex或者全局的事件驱动，然而废弃的这些方法在vux UI框架中很多地方都有使用，无疑在项目中用到它的地方在2.0版本都会不起作用，甚至会报错。

c.v-ref、v-el 弃用 统一使用ref属性为元素或组件添加标记，然后通过this.$refs获取

例如<p ref="a"></p>   获取方法为this.$refs.a 对于自定义组件同样适用

d.$els 是用来获取元素DOM对象，这个也废弃不用，$refs可以起到替代性作用。

e.v-for循环中常用的$index、$key也已不支持使用，trackby被key属性替换。

f.自定义组件中的partial，弃用，这个一直没用到

g.新增 v-once指令

h.新增 propsData

j.新增 render
