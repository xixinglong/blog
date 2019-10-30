
---

title: vue 基础知识学习

urlname: oev5yg

date: 2019-10-30 10:43:10 +0800

tags: []

---

1.MVC和MVVM 的区别？<br />
<br />![截图.png](https://cdn.nlark.com/yuque/0/2019/png/319940/1572403509120-1f91fad6-e14b-4d75-96cc-6f29f8ec9b45.png#align=left&display=inline&height=637&name=%E6%88%AA%E5%9B%BE.png&originHeight=637&originWidth=1545&search=&size=683817&status=done&width=1545)<br />2.学习了vue中最基本代码结构<br />
<br />![截图 (1).png](https://cdn.nlark.com/yuque/0/2019/png/319940/1572403517442-7e3fb6dc-8400-452d-96b7-81a581c12c24.png#align=left&display=inline&height=732&name=%E6%88%AA%E5%9B%BE%20%281%29.png&originHeight=732&originWidth=1129&search=&size=264047&status=done&width=1129)<br />
<br />3.插值表达式  v-cloak  v-text  v-html  v-bind(缩写是 ： )  v-on(缩写是 @)  v-model  v-for  v-if  v-show<br />v-cloak ：可以解决 插值表达式闪烁问题；<br />v-text   ：默认 v-text 是没有闪烁问题的，v-text 会覆盖元素中原本的内容，但是  插值表达式  只会替换自己的这个占位符，不会把整个元素的内容清空<br />v-html  ：<br />v-bind  ：简写“：”，绑定属性，可以写合法的表达式<br />v-on    ：简写“@” ，绑定事件<br />
<br />4.事件修饰符   .stop  .prevent  .captrue  .self  .once<br />.stop：阻止冒泡<br />.prevent：阻止默认事件<br />.captrue：添加时间侦听器时使用事件捕获模式<br />.self：只当事件在该元素本身（比如不是子元素）触发时触发回调<br />.one：事件只触发一次<br />.stop和.self区别？<br />.self 只会阻止自己身上冒泡行为的触发，并不会真正阻止 冒泡行为<br />
<br />5.el ：指定眼控制的区域  data ：是个对象，指定了控制的区域内要用到的数据  methods 虽然带个后缀，但是是个对象，这里可以自定义了方法<br />6.在vm实例中，如果要访问 data 上的数据，或者要访问 methods 中的方法，必须带this<br />7.在v-for 要会使用key 属性 （只接受 string / number）<br />8.v-model 只能应用于表单元素<br />9.在vue中绑定样式两种方式  v-bing：class  v-bind：style<br />class：<br />1.第一种方式，直接传递一个数组，注意这里 class 需要使用  v-bind  做数据绑定<br />2.第二种方式，在数组中使用三元表达式，提高代码的可读性 例如： ：class=“[ 'aa','bb',flag?'cc':'' ]”   (flag是true或者false)<br />3.第三种方式，在数组中使用 对象来代替三元表达式，提高代码的可读性  例如：  ：class=“[ 'aa','bb',{‘cc’：flag } ]”<br />4.第四种方式，直接使用对象  例如： ：class="{‘aa’:flag,active":true}“<br />style：<br />1.第一种方式，直接在元素上通过：style的形式，书写样式对象  ：style=“{color：‘red’，‘font-sitze’：‘40px’，‘font-weight’：‘200’}”<br />2.第二种方式，将样式对象，定义到data中，并直接引入到：style中  ：style=“dataStyle”  dataStyle：{color：‘red’，‘font-sitze’：‘40px’，‘font-weight’：‘200’}<br />3.第三种方式，在：style中通过数组，引入多个data上的样式对象 ：style=“[dataStyle,dataStype2]”<br />10.v-for<br />1.迭代数组<br />2.迭代对象中的属性<br />3.迭代数字<br />v-if 和 v-show的区别？<br />v-if 的特点：每次都会重新删除或创建元素。<br />v-show  的特点：每次不会重新进行DOM的删除和创建操作，只是切换了元素的display:none 样式<br />应用场景：<br />如果元素涉及到频繁的切换，最好不要使用v-if，而是推荐使用 v-show;<br />如果元素可能永远也不会被显示出来被用户看到，则推荐使用 v-if;

