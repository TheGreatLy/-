1.下面在控制台的输出是什么？？

```js
console.log([typeof null,null instanceof Object])
```

2.下面在控制台的输出是什么？？

```js
[]["map"]+[]
[]["a"]+[] 
[]['push'](1) 
(![]+[])[+[]] 
(![]+[])[+!![]] 
++[[]][+[]] + [+[]] 
[1 < 2 < 3, 3 < 2 < 1]
```

3.阅读以下代码，下面的输出是什么？？

```js
var a = 1,
    b = c = 0;
function add(n){
    return n=n+3;
}
y = add(a);
function add(n){
    return n=n*5;
}
z = add(a);
console.log(y,z);

```

4.阅读以下代码，下面的输出是什么？？

```js
function showCase(value) {
    switch(value) {
    case 'A':
        console.log('Case A');
        break;
    case 'B':
        console.log('Case B');
        break;
    case undefined:
        console.log('undefined');
        break;
    default:
        console.log('Do not know!');
    }
}
showCase(new String('A'));
        
```

5.以下代码在控制台的输出是什么??

```js
parseInt(3, 8)
parseInt(3, 2)
parseInt(3, 0)
```

6.以下代码在控制台的输出是什么??

```js
["1", "2", "3"].map(parseInt)
```

7.以下代码在控制台的输出是什么??

```js
function fn(ary) {
  ary[0] = ary[2];
}
function bar(a,b,c) {
  c = 10;
  fn(arguments);
  return a + b + c;
}
bar(1,1,1)
```

8..以下代码在控制台的输出是什么??

```js
function fn(){}
console.log(  Array.isArray(Array.prototype) ,Object.getPrototypeOf(fn) )
```

9.下面的输出是什么？？

```js
(function(){
  var x = y = 1;
})();
console.log(y);
console.log(x);
```

10.下面的输出是什么？？

```js
var	result = false===1;
console.log(result);
if(typeof c&&-true+ (+undefined)+''){
    console.log('l am ok');
}
if(22+'33'*2==88){
    console.log('我还能做十道');
}
!!' '+!!'' -!!false||console.log('我选择go die');
```

11.下面的输出是什么？？

```js
var length = 10;
function fn(){
    console.log(this.length);
}
var  obj = {
    length:5,
    method:function(fn){
        console.log(this.length);	//由obj调用  打印5
        fn();					//fn挂载在全局由windows调用 打印10	
        arguments[0]();		//实参列表的第零项执行 由arguments调用 arguments为数组[fn，1] 他的length为								2  故打印2 		
    }
}
obj.method(fn,1)
```

12.下面的代码输出是什么？？

```js
var a = { n:1 };		
var b = a;			
a.n = a = { m:1 };
console.log(a,b)

```

13.下面的代码输出是什么？？

```js
var x = 1
if(function fn(){}){
    x += typeof fn
}
console.log(x);
```

14.下面的代码输出是什么？？

```js
var x = 10;
function a(){
    y = function(){
        x = 2;
    }
    console.log(this);
    return function(){
        var x = 3;
        y();
        console.log(this.x);
    }.apply(this)
}
a();
console.log(y);

```

15.下面的代码输出是什么？？

```js
typeof undefined=== typeof Undefined
```

16.下面的代码输出是什么？？

```js
var a={},
b={key:'b'},
c={key:'c'};

a[b]=123;  //a["object Object"] = 123;
a[c]=456;  //a["object Object"] = 456;

console.log(a[b]) //456
```

17.下面的代码输出是什么？？

```js
var out = 25,
   inner = {
        out: 20,
        func: function () {
            var out = 30;
            return this.out;
        }
    };
console.log((inner.func, inner.func)());
console.log(inner.func());
console.log((inner.func = inner.func)());
```

18.下面的代码输出是什么？？

```js
if (!("a" in window)) {
    var a = 1;
}
alert(a);

```

19.下面代码的输出是什么？？

```js
var fn = function test(){
	console.log('代码执行了')
}
test()
```

20.下面的代码输出是什么？？

```js
var str = typeof typeof {name:'heaven'};
if( str.length==6 ){
	str.prop = '这是一波字符串';
}
console.log(str.prop)
```

21.下面的代码输出是什么？？

```js
function fun(n,o) {
    console.log(o);
    return {
        fn:function(m){
            return fun(m,n);
        }
    };
}

var a = fun(0);	
a.fn(1); 
a.fn(2); 
a.fn(3); 
var b = fun(0).fn(1).fn(2).fn(3);
var c = fun(0).fn(1); 
c.fn(2);	
c.fn(3);
```

22.下面的代码输出是什么？？

```js
var a = 1;
var b = 2[a,b] = [b,a]
console.log(a,b)
```

23.下面的代码输出是什么？？

```js
var n = 10;
var obj = {
    n : 5,
    c : a()
};
function a(){
	var n = 7;
    var c = function(){
        var n = 3;
        console.log(this.n)
    }
    return c;
};
obj.c()			

```

24.下面的代码输出是什么？？

```js
var arr = [1,3,5,7,9];
function fn(){
    this.arr = [2,4,6,8,10];
    arr.forEach( function(){
        console.log(this.arr);
    } );
}
new fn()
```

25. 下面的代码输出是什么？

    ```js
    function test (){
        var n = 4399;
        function add(){
            n ++;
            console.log(n)
        };
        return {
            n,
            add
        }
    }
    var result1 = test();
    var result2 = test();
    result1.add();
    result1.add();
    console.log(result1.n);
    result2.add();
    
    ```
