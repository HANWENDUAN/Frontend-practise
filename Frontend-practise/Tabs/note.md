3 functions: hover,active,hiden content. 
1. ***.addEventListener*** can add mutliple event.
2. ***onclick*** cant. latest one will overwrite. it wont work. (***using inline is not be recommended***)


    var h = document.getElementById('a');
    1. h.onclick = doThing_1;
    2. h.onclick = doThing_2;

    3. h.addEventListener('click', doThing_3);
    4. h.addEventListener('click', doThing_4);
3. Some JS framwork like Angular has function:
    <button (click)="doSomething()">Do Something</button><br>
    looks like inline event but not. Could be addEvent.
4. use ***overflow:hidden*** to restrict the scrollbar showing up.

5. **作用域！！！！** 函数中声明的var是全局变量所以<br>
   这个是块状作用域和词法作用域.
```
for(var i = 0; i < 5; i++) {
  setTimeout(function() {
     console.log(i);			// 5 5 5 5 5
  }, 200);
};

```
因为词法作用域的原因。var i全局只有一个值。所以是5 全部执行完之后的数值 莺歌用let i=0；。


1. fade in tag
```
.tabcontent {
  animation: fadeEffect 1s; 
}


@-webkit-keyframes fadeEffect {
  from {opacity: 0;}
  to {opacity: 1;}
}

@keyframes fadeEffect {
  from {opacity: 0;}
  to {opacity: 1;}
}
```