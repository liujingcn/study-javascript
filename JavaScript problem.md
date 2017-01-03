**1. 问题一：**
```
        var foo = function foo(){
        console.log(foo === foo);
    };
    foo();
```
结果为：==true==

---
**2. 问题二：**
```
function aaa(){
		return //
		{
		    test : 1
		};
	}
	console.log(typeof aaa());
```

输出结果为：==undefined==

---
**3. 问题3：**   

```
console.log(Number("1")-1 == 0);
```
输出结果为：==true==


---
**4. 问题4：**

```
console.log((true + false) > 2 + true);
```
输出结果为：==false==

**5. 问题5：**

```
function bar(){
		return foo;
		foo = 10;
		function foo(){}
		var foo = '11';
	}
	console.log(typeof bar());
```
输出结果为：==function==

**6. 问题6：**

```
console.log("1" - - "1");
```
输出结果为：==2==

**7. 问题7：**

```
var x = 3;

	var foo = {
		x :2,
		baz:{
			x:1,
			bar:function(){
			return this.x;
			}
		}
	}

	var go = foo.baz.bar;

	console.log(go());//this指向window
	console.log(foo.baz.bar());//this指向当前对象
```
输出结果为：==3和1==


---
**8.问题8：**

```
console.log(new String("This is a string") instanceof String);
```
输出结果为：==true==

---
**9.问题9：**

```
console.log([]+[]+'foo'.split(''));
```
split() 方法用于把一个字符串分割成字符串数组。如果把空字符串 ("") 用作 separator，那么 stringObject 中的每个字符之间都会被分割。  

输出结果为：==f,o,o==


---
**问题 10：**

```
console.log(new Array(5).toString());
```
输出结果为：==,,,,==

---
**问题 11：**

```
var myArr = ['foo', 'bar', 'baz'];
	myArr.length = 0;
	myArr.push('bin');
	console.log(myArr);
```
输出结果为：==["bin"]==

---
**问题 12：**

```
console.log(String('Hello')==='Hello'); 
```
输出结果为：==true==

---
**问题 13：**

```
var x = 0;
	function foo() {
	    x++;
	    this.x = x;
	    return foo;
	}
	var bar = new new foo;
	console.log(bar.x); 
```
输出结果为：==undefined==

---
**问题 14：**

```
console.log("This is a string" instanceof String)
```
instanceof 运算符可以用来判断某个构造函数的prototype属性是否存在另外一个要检测对象的原型链上。
  
  输出结果为：==false==
  
  ---
**问题 15：**

```
var bar = 1,
   	 	foo = {};

	foo: {
	    bar: 2;
	    baz: ++bar;
	};
	
	console.log(foo.baz + foo.bar + bar);
```

  因为console.log(foo),foo为空对象
  
  输出结果为：==NaN==
  


---
**问题 16：**

```
var myArr = ['foo', 'bar', 'baz'];
	myArr[2];
	console.log('2' in myArr);
```

  输出结果为：==true==
  

---
**问题 17：**

```
var arr = [];
	arr[0]  = 'a';
	arr[1]  = 'b';
	arr.foo = 'c';
	console.log(arr.length);
```

  输出结果为：==2==
  

---
**问题 18：**

```
function foo(a, b) {
	    arguments[1] = 2;
	    alert(b);
	}
	foo(1);
```

  输出结果为：==undefined==

---
**问题 19：**

```
console.log(NaN === NaN)
```

  输出结果为：==false==
 
 ---
**问题 20：**

```
console.log(10 > 9 > 8 === true)
```

  输出结果为：==false==