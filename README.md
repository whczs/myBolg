
# 浅谈事件
事件流:描述的是从页面中接收事件的顺序。
事件三个阶段：捕获、目标、冒泡
### DOM0 级事件
方法指定的事件处理程序被认为是元素的方法。
### DOM2 级事件：
DOM2级事件定义了两个方法，addEventListener()和removeEventListener()分别用于指定和删除事件。所有DOM节点中都包含这两个方法，并且它们都接受3 个参数：要处理的事件名、作为事件处理程序的函数和一个布尔值。最后这个布尔值参数如果是true，表示在捕获阶段调用事件处理程序；如果是false，表示在冒泡阶段调用事件处理程序。
##### addEventListener()示例：
```js
var btn = document.getElementById("myBtn");
btn.addEventListener("click", function(){
alert(this.id);
}, false);
btn.addEventListener("click", function(){
alert("Hello world!");
}, false);
```
##### removeEventListener()示例：
```js
var btn = document.getElementById("myBtn");
btn.addEventListener("click", function(){
alert(this.id);
}, false);
btn.addEventListener("click", function(){
alert("Hello world!");
}, false);
```
* IE事件处理程序
