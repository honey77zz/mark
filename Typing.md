# js原生实现打字效果
## 方法一
```javascript
var Div=document.getElementById('typing')
var str='忽如一夜春风来，千树万树梨花开。'
function typing(){
    var i=0;
    if(i<str.length){
        Div.innerHTML=str.slice(0,i++)+'_'
        setTimeout('typing()',200)

    }else{
        Div.innerHTML=str
    }
}
typing()
```
## 方法二
``` javascript
function Typing(){
    var Div=document.getElementById('typing')
    var str='忽如一夜春风来，千树万树梨花开。'
    var contentArr=str.split('')
    var content=''
    var index=0
    var timer=setInterval(function(){
        content+=contentArr[index]
        Div.innerHTML=content+'_'
        index++
        if(index===contentArr.length){
        Div.innerHTML=content
        clearInterval(timer)
        }
    },200) 
}

Typing()

```

> 备注：章鱼是个是傻子

共同体**拖拖**拖拖过