# JavaScript面向对象

声明对象方式一:

```javascript
var person={
    name:"lucas",
    age:30,
    eat:function(){
        alert("能吃");
    }
}
```

声明对象方式二：

```javascript
function Person(){
    
}
Person.prototype = {
    name:"lucas",
    age:30,
    eat:function(){
        alert("老子在吃法");
    }
}
var p = new Person();
p.age = 40;
```

## 面向对象深入

* js中并没有类这一概念

```javascript
function Person(){
    var _this = {}
    _this.sayHello = function () {
        alert("hello");
    }
    return _this;
}

function Teacher(){
    var _this = Person();
    var superSay = _this.sayHello;
    _this.sayHello = function(){
        superSay.call(_this);
        alert("tHello");
    }
    return _this;
}

var t = Teacher();
t.sayHello();

```

