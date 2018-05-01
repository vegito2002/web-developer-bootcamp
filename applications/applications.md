### lec85,86 js console
js is the *verb*. 
<img src="https://www.dropbox.com/s/cafmvqcr56a13l8/Screenshot%202018-04-30%2015.47.29.png?raw=1" width="400">
not usually used often. just some in place interaction or debugging. just like how you can change the css in place, you can change the js behavior in place too. 

### lec87,88,89,90,91,92,93,94,95,96
js does not differentiate float and integers: just all are numbers. `null` and `undefined` are also values, not types.   
js console is some repl environment. type a number and it echos back. 
```
1 / 3
0.3333333333333333
```
so there is no integer division.   
single or double quotes work both. but need to match. if you want apostrophe, then use double quotes, or use escape. `.length` attribute, not quite like java. can do `"hello"[0]` like C++. the length is same semantics as java rather than C++. 
```js
var i = 1
undefined
```
so `var` is also a function with return value of `undefined`? 

```js
var num
undefined
num
undefined
```
so a var with no type is also `undefined`. `null` means not having value, not not defined. `null` just means complete emptiness. 

built-in methods. `clear()` clears the console. `alert("hello")`. `alert(1+2)`. can be used like `print` to debug. `console.log("dkja")` is the actual print in console. `prompt ("please input your name: ")`, then you get a popup for input. returns the value inputed, so you can store it. 

```html
<head>
    <title>Script Demo</title>
    <script src="lec92.js"></script>
</head>
```
link the file here. note that the attribute is `src` not the default `type`. 

都是比较无聊的东西, 我就记录一些关键词, 练习什么的都懒得跟着打了; 

`script` after this `h1`, so your js application will run after the `h1` loads:
```html
<!DOCTYPE html>
<html>
<head>
    <title>Age Calc</title>
</head>
<body>
<h1>Age Calc Solution</h1>

<script type="text/javascript" src="calc.js"></script>
</body>
</html>
```

### lec97, 98, 100, 101, 102, 103
`===`: equal value **and** type. 
```js
var x = 5
undefined
x == "5"
true
x === "5"
false
```
<img src="https://www.dropbox.com/s/zqh2512eedupaol/Screenshot%202018-04-30%2019.03.48.png?raw=1" width="400">
one is string, one is a value. `===` is more specific and usually more preferred. 
<img src="https://www.dropbox.com/s/mxz4u9pbuhioce8/Screenshot%202018-04-30%2019.04.53.png?raw=1" width="400">
<img src="https://www.dropbox.com/s/lbb4ly703ygquvx/Screenshot%202018-04-30%2019.05.38.png?raw=1" width="400">
这个就有点不讲理了, 我还以为是类似c++的那个规则; `NaN` is not comparable to `NaN`, quirks of implementation. 
```js
true == "1"
true
true == "11"
false
true == "2"
false
var x = 3
undefined
x == "3"
true
```
if you want to find the truthy/falsy value of a non-boolean:
<img src="https://www.dropbox.com/s/x2nllhix1mscp9w/Screenshot%202018-04-30%2019.12.39.png?raw=1" width="400">
use the `!` to coerce it to boolean. if you don't like reading negated value, do it twice. hard rules:
<img src="https://www.dropbox.com/s/oe5rsw0rmhrylxg/Screenshot%202018-04-30%2019.13.00.png?raw=1" width="400">
note how `NaN` jumps in right now. 
```js
!!"false"
true
```

```js
1 == "1"
true
1 === "1"
false
```
again, `==` performs **type coercion**, and may cause unexpected result. in this case, which is promoted? int to string or string (parsed) to int? I think the former: in a way string provides more precision.  

```js
// If age is a perfect square
if(age % Math.sqrt(age) === 0) {
  console.log("Your age is a perfect square!");
}
```
这样判断也行吧. 反正如果想到直接算sqrt, 后面办法就很多了; 
```js
Math.sqrt (3)
1.7320508075688772
3 / Math.sqrt (3)
1.7320508075688774
```
这个是不是有点不讲理了...所以js的mod到底是怎么运行的? 

> Why does 49.90 % 0.10 in JavaScript return 0.09999999999999581? I expected it to be 0.

> Because JavaScript uses floating point math which always leads to rounding errors.  
>   
> If you need an exact result with two decimal places, multiply your numbers with 100 before the operation and then divide again afterwards:  
>   
> var result = ( 4990 % 10 ) / 100;  

有点无语. 反正这种不知道什么semantic的到左还是避免, 完全无法预测结果; 
```js
var p = prompt ()
undefined
p
"dklja"
```
`prompt` returns a string, which is not really so surprising: standard in most languages. 
```js
var num = prompt()
undefined
num
"12"
Number(num)
12
```
this is useful when you want to do `===` on the result you have, against say `12` itself: string won't work. 

### lec105, 106, 107, 108, 109, 111, 112, 113, 114
> Meanwhile, be warned that if you write an infinite loop and run it, it could crash your browser and possibly even your computer. 

playing repl on browser can be dangerous. 
<img src="https://www.dropbox.com/s/3f5ujm6j93usuls/Screenshot%202018-04-30%2019.33.47.png?raw=1" width="400">
跟java没有太大区别; 

### lec115, 116, 117, 118, 119, 120, 121, 122, 123
<img src="https://www.dropbox.com/s/pousfotolfxodbo/Screenshot%202018-04-30%2019.37.35.png?raw=1" width="400">
<img src="https://www.dropbox.com/s/y7x92eo383d5a4g/Screenshot%202018-04-30%2019.38.48.png?raw=1" width="400">
no type information. 
<img src="https://www.dropbox.com/s/487penbseqr0b4y/Screenshot%202018-04-30%2019.39.33.png?raw=1" width="500">
好像`console.log`自动换行. 
<img src="https://www.dropbox.com/s/5onkurjtbjjl8l5/Screenshot%202018-04-30%2019.40.53.png?raw=1" width="400">
这个`slice`好像就是`substring`的意思; 然后`charAt`一样的. 
<img src="https://www.dropbox.com/s/qcayhrxjm1ye06n/Screenshot%202018-04-30%2019.42.16.png?raw=1" width="400">
so you can use `typeof`. 
<img src="https://www.dropbox.com/s/klu893robnu1p5c/Screenshot%202018-04-30%2019.42.35.png?dl=0" width="500">
两种声明方式, 这个有点像OCaml那个, 第一种就是直接把函数名字放在signature里面, 第二种就是用一个assign an anonymous function to var的感觉; 注意他的解释, 一个是declaration, 一个是expression, 这样理解也是不错的; 

<img src="https://www.dropbox.com/s/pln0b0tl50oge9e/Screenshot%202018-04-30%2019.47.35.png?raw=1" width="400">
整个syntax还是跟java非常类似的, 包括这个`replace`也是一个返回值而不是mutation. 注意js里面这个regex的写法好像有点奇怪; 

<img src="https://www.dropbox.com/s/jnft6gfckb9mdwl/Screenshot%202018-04-30%2019.49.03.png?raw=1" width="400">
这个跟OCaml好像啊, 直接就是向上找. 不对, 自己傻逼了, 这个就跟global var一样的吧, 没有什么神奇的. 

<img src="https://www.dropbox.com/s/iy6n957lpweeu2i/Screenshot%202018-04-30%2019.52.51.png?raw=1" width="400">
这个好奇怪啊, 这个如果是java肯定就报错了, 这里直接就悄悄的返回一个undefined就拉倒了; 所以undefined到底代表什么? 

### lec124, 125, 126, 127
好像有两个函数, `setInterval` and `clearInterval`, 就是higher order function, 具体怎么用的还不太清楚; 
<img src="https://www.dropbox.com/s/7m5arypdwrn5qwa/Screenshot%202018-04-30%2019.57.19.png?raw=1" width="500">

<img src="https://www.dropbox.com/s/jylhya0tbz347th/Screenshot%202018-04-30%2019.59.54.png?raw=1" width="500">
这个就跟Python很像; 但是也保留了java的`new`. 

<img src="https://www.dropbox.com/s/888k806q12idjbu/Screenshot%202018-04-30%2020.00.54.png?raw=1" width="400">
看起来好像js的array是什么操作都有了; string也有, stack这种也有; 

```js
var ar1 = [1,2,3]
undefined
var ar2 = [4]
undefined
ar1 + ar2
"1,2,34"
```
这个有点奇怪. 反正就是Python的这个append没有在`+`里面实现的意思, 你这样写他就干脆直接全都promote到string来处理, 类似于`ar1.toString () + ar2.toString()`. 
```js
ar1.concat (ar2)
(4) [1, 2, 3, 4]
ar1
(3) [1, 2, 3]
ar2
[4]
```
这样也好, 还是挺舒服的. 另外注意这里`concat`也是一个immutable的操作; 这个也要熟悉一下; 
```js
ar1.push (5)
4
ar1
(4) [1, 2, 3, 5]
```
c++风格的这些API; 

<img src="https://www.dropbox.com/s/b5bjp2hjd8sxubp/Screenshot%202018-04-30%2020.05.44.png?raw=1" width="400">
这个稍微注意一下, `push`和`pop`还是类似Stack的操作, 不过这里操作位置是在end, 也就是认为end是实际的栈顶. 这个实际上跟c++是有一点区别的; c++我记得实际上如果你真的是想tail使用, 是要用`push_back`还是什么的, 而不是`push`. 

另外注意这两个函数的返回值, `push`返回长度, `pop`返回的自然是被pop出来的东西; 

`shift`, `unshift`跟push/pop完全类似, 只不过这两个是在head操作; 
<img src="https://www.dropbox.com/s/als9t7tyx4qx73j/Screenshot%202018-04-30%2020.08.35.png?raw=1" width="400">
另外这个命名也有点奇怪, 结果unpush实际上是一个put的操作; 

```js
ar1
(4) [1, 2, 3, 5]
ar1.unshift (0)
5
ar1
(5) [0, 1, 2, 3, 5]
```
仍然是mutation操作, 这个也是符合java的习惯的;  

<img src="https://www.dropbox.com/s/5yi4bropcqpmgko/Screenshot%202018-04-30%2020.10.38.png?raw=1" width="400">
基本是跟substring差不多的语义, 同样是immutable. 

另外, 虽然我讲的时候, 是把push/pop and shift/unshift分开讲, 好像以为是两个各自是一套Stack操作, 但是你要看出来这里实际上整个array是可以实现一个Deque的功能, 或者说双链表(这个效率可能差一点)的完整的功能的. 这个也是为什么老师只讲了这几个函数. 

### lec128, 129, 130
```js
ar1
(5) [0, 1, 2, 3, 5]
ar1[ar1.length]
undefined
```
出界也不报错. 

> Chrome browser behaves a little strangely when using alert, prompt, or confirm functions. It doesn't display the HTML on the page until after the popup has been closed. This is problematic since our HTML contains instructions for the user to be able to use the app we're building.  
>   
> You can avoid this by wrapping your JS code in the following setTimeout function:  

```js
  window.setTimeout(function() {
      // put all of your JS code from the lecture here
  }, 500);
```

> 
> This gives the HTML a half second to load before running the JS, which circumvents the issue of the prompt function blocking the HTML from loading right away.  
>   
> This is not something you would have to deal with in the real world as prompt, alert, and confirm functions are almost never used and when they are it's typically not on page load.  
>   
> You'll also learn jQuery in latter sections which has a cool $('document').ready()  function that you could use in place of the window.setTimeout workaround mentioned above.  
>   
> Note, if you want to be able to access the todos variable from the chrome developer console then you'll need to put it in the global scope, see example below:  

```js
var todos = ["Buy New Turtle"];  
window.setTimeout(function() {  
    // put all the rest of your JS code from the lecture here  
}, 500);  

```
> If you include the todos array inside of the window.setTimeout() function then it's scope will be local to the anonymous function (callback) and you won't be able to access it from the chrome console.  

这一期要求做一个todo list, 但是是一个很无聊的功能能, 懒得跟着敲了; 

```js
console.log (ar1)
VM110:1 (5) [0, 1, 2, 3, 5]
```
这个array print做的倒是还可以; 
<img src="https://www.dropbox.com/s/2j21u8ujpqsglj4/Screenshot%202018-04-30%2020.25.04.png?raw=1" width="500">
see how you can actually query even variables in the console. this is great for debugging. 

### lec131, 132, 133
讲到这里为止, 实际上还都是针对js本身的编程, 当然浏览器提供了IO. 真正我们最后想要达到的效果是, js执行之后能够对页面的html进行一个修改, 这个目前还没有讲到; 

<img src="https://www.dropbox.com/s/ttc2gkd0zco1ix7/Screenshot%202018-04-30%2020.29.05.png?raw=1" width="400">

这个跟java的foreach还有点区别. 这个要传一个function进去的; 另外可以看到, 这里的forEach, 实际上是一个函数, 而java里面, 实际上最后好像就是一个语法糖, 底下还是用iterator实现的. 
<img src="https://www.dropbox.com/s/5sgninhzpqfbafh/Screenshot%202018-04-30%2020.32.59.png?raw=1" width="400">
单纯看这里, 是不是可以说undefined实际上跟void差不多? 所以报错的时候, 返回值也是直接返回一个类似void的东西? 

> .forEach takes a callback function, that callback function is expected to have at least 1, but up to 3, arguments. This is how .forEach was designed.  
>   
> The arguments are in a specific order:  
> - The first one represents each element in the array (per loop iteration) that .forEach was called on.  
> - The second represents the index of said element.  
> - The third represents the array that .forEach was called on (it will be the same for every iteration of the loop).  
>   
> You have a couple options when calling .forEach on an array:  
>   
> You can pass in an anonymous function:  

```js
[1,2,3].forEach(function(el, i, arr) {
  console.log(el, i, arr);
});
```

> Or you can pass in a pre-written, named function.

```js
function logNums(el, i, arr) {
  console.log(el, i, arr);
}

 
[1,2,3].forEach(logNums);
```

> Notice how in the second example we don't invoke logNums when passing it into .forEach? We simply pass in the function name. We don't need to invoke the logNums function, .forEach does that for us. In fact, it invokes the function multiple times, once for every element inside of the array.

[todos.html](todos.html), [todos.js](todos.js)

大概自己看看吧, 不能直接改变页面内容的这些, 都懒得看了; 

```js
ar1
(5) [0, 1, 2, 3, 5]
(anonymous) @ VM121:1
ar1.splice (1, 1)
[1]
ar1
(4) [0, 2, 3, 5]
```
注意这个splice的用法; 跟string的那个`slice`不要搞混了; 另外这个splice函数是一个mutation的函数; 第一个参数是index, 第二个是一共要splice掉的count, 跟slice的参数也有不同. 













































