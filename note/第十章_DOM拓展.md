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
