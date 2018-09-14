# Dom拓展

## querySelector()
* 接收一个css选择器,返回与该模式匹配的第一个元素，如果没找到，返回null

## querySelectorAll()
* 接收一个css选择器,返回与该模式匹配的所有元素（NodeList实例），
* 如果没找到，返回null
* 返回的是NodeList的一个快照，而不是一直对文档进行动态查询的返回

## matches
* 接收一个参数(Css选择符),如果调用者元素与该选择符匹配，返回true，否则false

## 元素遍历
>Element Traversal API为DOM元素添加了以下5个属性
1. childElementCount 返回子元素的个数
2. firstElementChild  指向第一个子元素;
3. lastElementChild 指向最后一个元素
4. previousElementSibling 指向前一个兄弟元素
5. nextElementSibling 指向后一个兄弟元素
> 遍历的Demo
```javascript
var i, len , child = element.firstElementChild;
while(child != element.lastElementChild) {
    processChild(child);
    child = child.nextElementSibling;
}
```
## HTML5
1. getElementsByClassName 根据类名返回NodeList集合
2. NodeList 元素增加 classList属性，可以通过 .add() .remove(), contains(), toggle() 来更方便的操作class
3. document.activeElement 当前获取了焦点的元素(一般都是body)
4. 可以为元素添加 自定义数据属性，但是要以 data- 开头
> demo
```html
<div id="myDiv" data-appId="12345" data-myname="Jack">
```
```javascript
var div = document.getElementById('myDidv');
// get
var appId = div.dataset.appId;
var myName = div.dataset.myname;
// set
div.staset.appId = 'newValue';
```
5. outHTML 返回调用者及其子节点的HTML标签

>注意操作dom时的内存与性能问题,删除元素前，先手删除被删元素的所有事件处理程序.

6. children 属性 （HTMLCollection)实例
7. contains(El) 方法， 返回调用者是否包含参数的El
8. scrollIntoView() 将调用者滚动到视图窗口可见
9. 
