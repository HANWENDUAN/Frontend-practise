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
