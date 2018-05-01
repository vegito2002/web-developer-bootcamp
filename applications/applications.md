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
<img src="https://www.dropbox.com/s/klu893robnu1p5c/Screenshot%202018-04-30%2019.42.35.png?raw=1" width="500">
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

### lec135, 136, 137
<img src="https://www.dropbox.com/s/w2jzgpa6j3lznfe/Screenshot%202018-04-30%2020.50.21.png?raw=1" width="400">

看这里, foreach也是有坑的. 他这个return最后只是return掉了一个element的函数执行, 下一个element还是会继续执行这个无名函数. 这个应该是可以修正的, 不过应该很麻烦; 

<img src="https://www.dropbox.com/s/n283dq072c9617f/Screenshot%202018-04-30%2020.51.30.png?raw=1" width="400">
sum的foreach写法; 这个手感可能稍微有点陌生. 

```js
// =========
// VERSION 1
// =========
function myForEach(arr, func){
    for (var i = 0; i < arr.length; i++) {
        func(arr[i]);
    }
}

var colors = ["red", "orange", "yellow", "green", "blue", "PURPLE"];
myForEach(colors, function(color){
    console.log(color);
});

// =========
// VERSION 2 
// =========
Array.prototype.myForEach = function(func){
  for(var i = 0; i < this.length; i++) {
   func(this[i]);
  }
};

var colors = ["red", "orange", "yellow", "green", "blue", "PURPLE"];
colors.myForEach(function(color){
    console.log(color);
});
```
prototype好像就有点类似an object that stores the collections of all attributes/methods这样的东西; 不过难道可以直接用户也修改`Array`的属性? 要是只是修改一个array object本身而不是type的我倒还可以接受; 

另外, 注意这里这个`this`的使用; 

### lec138, 139, 140, 141, 142, 143
<img src="https://www.dropbox.com/s/5ukn02dleof8b3g/Screenshot%202018-04-30%2021.02.51.png?raw=1" width="500">
array is not good because we don't need the *order*, but rather than the *mapping*. for example, you can't enforce name to be index 0. 

<img src="https://www.dropbox.com/s/52gd7rp9tp90la6/Screenshot%202018-04-30%2021.03.54.png?raw=1" width="400">
所以居然也可以用跟array一样的做法来搞. 不过要用string, 还是有点奇怪; 

<img src="https://www.dropbox.com/s/ly3b6f715opqzzq/Screenshot%202018-04-30%2021.05.04.png?raw=1" width="600">
但是好像用string的方法更好, 一来是这个field name的自由度更高, 而来是允许dynamic, 这个就很强了; 

<img src="https://www.dropbox.com/s/j0qb14yjw9u3lj1/Screenshot%202018-04-30%2021.06.51.png?raw=1" width="600">
甚至根本就不需要定义, 后面自己临时去加; 另外一个奇怪的刚才没注意的: 你看object定义里面, field之间居然是用逗号来分开的; 

<img src="https://www.dropbox.com/s/pl1gfzslec8ktov/Screenshot%202018-04-30%2021.09.19.png?raw=1" width="600">
这个一看, js的array和object完全就是JSON的格式. 难怪. 之前我一直认为大括号代表的是dictionary, 当时这么理解是可以的, 不过放在js自己的语境下面理解, 实际上应该是大括号代表object. 

另外之前说过, 如果想要用dot, 那么field name开头不能是数字: 一个解决办法就是用underscore. 当然这个也是一个规避的方法而已; 

<img src="https://www.dropbox.com/s/gmpoxsxk1gh41q8/Screenshot%202018-04-30%2021.13.45.png?raw=1" width="600">

<img src="https://www.dropbox.com/s/avw3xzn0qhbl9fs/Screenshot%202018-05-01%2001.14.52.png?raw=1" width="500">
function can also be a member, or a method. 
```js
obj.add (10, 5);
```
<img src="https://www.dropbox.com/s/vk3jrdru9fc6wmg/Screenshot%202018-05-01%2001.16.52.png?raw=1" width="400">

### lec144, 145, 148
[http://underscorejs.org/](http://underscorejs.org/)

<img src="https://www.dropbox.com/s/7rjvvtktv0w0yco/Screenshot%202018-05-01%2001.20.52.png?raw=1" width="400">
note how now this anonymous function does not need argument anymore. 

> As you begin working with the DOM you'll be writing some JavaScript code that selects HTML elements from the page and manipulates them.   
>   
> When doing this, be sure to include your JavaScript code at the bottom of the HTML document, right before the closing </body>  tag.  
>   
> The HTML will need to have loaded before the JavaScript is run, otherwise the JavaScript will throw an error because the HTML that it is trying to select and manipulate doesn't exist (yet).  

终于开始互动了. 

DOM: document object model. 

<img src="https://www.dropbox.com/s/eyid86ea2gk1942/Screenshot%202018-05-01%2001.27.19.png?raw=1" width="500">

each element turned into an object. 

<img src="https://www.dropbox.com/s/67o3kdibaq3b15d/Screenshot%202018-05-01%2001.28.22.png?raw=1" width="400">
this does not get the `document`, it's been hidden by the browser. 
<img src="https://www.dropbox.com/s/qnph1br22meg1of/Screenshot%202018-05-01%2001.29.07.png?raw=1" width="400">
this works, you see an object. 

so js is not scripting: I thought it just generates HTML files for us. 

<img src="https://www.dropbox.com/s/xubs216sstvmd0y/Screenshot%202018-05-01%2001.32.58.png?raw=1" width="500">

<img src="https://www.dropbox.com/s/1prgp8migs6drcy/Screenshot%202018-05-01%2001.34.04.png?raw=1" width="500">
so `querySelector` 返回的实际上是一个指针? 
<img src="https://www.dropbox.com/s/zrj2cvakzv8713g/Screenshot%202018-05-01%2001.34.58.png?raw=1" width="500">

### lec149, 150, 151, 152, 153
<img src="https://www.dropbox.com/s/rd5abgbtycrlcdq/Screenshot%202018-05-01%2001.38.17.png?raw=1" width="400">
<img src="https://www.dropbox.com/s/g3r8ohgyldw68q2/Screenshot%202018-05-01%2001.38.39.png?raw=1" width="400">
<img src="https://www.dropbox.com/s/gapqoelqiny7jls/Screenshot%202018-05-01%2001.41.46.png?raw=1" width="400">
remember that an `id` can appear at most one time in a page. 
<img src="https://www.dropbox.com/s/y1cjlf3okuwxv10/Screenshot%202018-05-01%2001.45.26.png?raw=1" width="500">
looks like an array, can bracket index, but not really an array. for instance, can't `forEach`. it's actually an object.  
<img src="https://www.dropbox.com/s/7jgxu9bygt2vg1n/Screenshot%202018-05-01%2001.46.59.png?raw=1" width="500">
returns a list no matter how many matches.  
<img src="https://www.dropbox.com/s/mke6xiuxeioaqi4/Screenshot%202018-05-01%2001.48.31.png?raw=1" width="500">
you can anything you would put in a css. it will always only return the first matche though. tag names also works of course. 
<img src="https://www.dropbox.com/s/vu03xfb1huqha3l/Screenshot%202018-05-01%2001.50.18.png?raw=1" width="400">
the last one returns `null` because we don't have any on this page.  
<img src="https://www.dropbox.com/s/vul0sicljlzle83/Screenshot%202018-05-01%2001.51.28.png?raw=1" width="400">

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>My Title</title>
</head>
<body>
    <h1>I am an h1!</h1>
    <p id="first" class="special">Hello</p>
    <p class="special">Goodbye</p>
    <p>Hi Again</p>
    <p id="last">Goodbye Again</p>
</body>
</html>
```

<img src="https://www.dropbox.com/s/zz44ihb5qo8ogo5/Screenshot%202018-05-01%2001.53.57.png?raw=1" width="500">
<img src="https://www.dropbox.com/s/wlee600212abo1i/Screenshot%202018-05-01%2001.54.42.png?raw=1" width="500">

<img src="https://www.dropbox.com/s/3k1x3zd6xk1fv8s/Screenshot%202018-05-01%2001.55.52.png?raw=1" width="500">
<img src="https://www.dropbox.com/s/ejjl72y8rhxskod/Screenshot%202018-05-01%2001.56.25.png?raw=1" width="500">
do note that all the values MUST be a string. 

each element has `style` property, which is huge. 
<img src="https://www.dropbox.com/s/qb7gv76wotmq2at/Screenshot%202018-05-01%2001.57.49.png?raw=1" width="400">

<img src="https://www.dropbox.com/s/njcztu23w61uv1w/Screenshot%202018-05-01%2002.00.04.png?raw=1" width="500">
这个技巧还是有点意思的; 不要自己手动去改这些property, 而是事先就在css里面用一个class把这个给打包起来; 如果你要改的时候, 直接改`class` of this element, 而不是一个一个的改所有的Property, 这样方便的多; 
<img src="https://www.dropbox.com/s/vqg2z786ywb12qy/Screenshot%202018-05-01%2002.01.53.png?raw=1" width="400">

<img src="https://www.dropbox.com/s/4khqms0oli29xm1/Screenshot%202018-05-01%2002.02.49.png?raw=1" width="400">
do note that this list is not an array, so you can't use `push` etc. you have to use `add`, `remove` etc. 

### lec154, 155
<img src="https://www.dropbox.com/s/weg3vsa64ek2qnh/Screenshot%202018-05-01%2002.04.57.png?raw=1" width="400">
<img src="https://www.dropbox.com/s/6yr9e5g1gdhb12i/Screenshot%202018-05-01%2002.06.14.png?raw=1" width="400">
<img src="https://www.dropbox.com/s/4zlvwqgych5yzio/Screenshot%202018-05-01%2002.06.35.png?raw=1" width="400">
note how all tags are removed, and all texts are *concatenated* as a string. 
<img src="https://www.dropbox.com/s/l8ocj7vcpjasdlr/Screenshot%202018-05-01%2002.07.40.png?raw=1" width="400">
completely overrides it, including any tags included in the text content. be aware of this danger. 
<img src="https://www.dropbox.com/s/hi9ooxxzko5ure6/Screenshot%202018-05-01%2002.08.27.png?raw=1" width="400">
<img src="https://www.dropbox.com/s/9tt9jgfe7vc9pr7/Screenshot%202018-05-01%2002.09.02.png?raw=1" width="400">
感觉后面就要开始直接的string scripting了;
<img src="https://www.dropbox.com/s/4aw7hxriqzv70kz/Screenshot%202018-05-01%2002.10.03.png?raw=1" width="400">
chaining works. 
<img src="https://www.dropbox.com/s/l16iu0za72k1vh6/Screenshot%202018-05-01%2002.11.11.png?raw=1" width="400">
<img src="https://www.dropbox.com/s/7qgka7auy52x5ru/Screenshot%202018-05-01%2002.11.44.png?raw=1" width="400">
`textContent` treats everything as string rather than html: it does not render it. `innerHTML` can work.  

<img src="https://www.dropbox.com/s/wsph2dminyp40rv/Screenshot%202018-05-01%2002.12.40.png?raw=1" width="400">

one subtle thing, use *attribute* to refer to things in html like `src`, but use *property* to refer to things like *border*. 

<img src="https://www.dropbox.com/s/z5bh07g9s6upnl2/Screenshot%202018-05-01%2002.15.44.png?raw=1" width="400">
note how he uses the returned array to access something like *the 2nd image*, rather than specifying the css selector. this is easier. 
<img src="https://www.dropbox.com/s/cvh113fwwlbt6m7/Screenshot%202018-05-01%2002.17.07.png?raw=1" width="400">
important to include the `http://`, otherwise it's treated as a relative path. this is just like unix fs. 
<img src="https://www.dropbox.com/s/3y9kvjkxesemlrl/Screenshot%202018-05-01%2002.18.04.png?raw=1" width="400">
now it's entirely changed. 

### lec156, 157
inspect then select trick to play with other people's website. 
<img src="https://www.dropbox.com/s/uuy0l4yjxp195au/Screenshot%202018-05-01%2002.21.59.png?raw=1" width="400">
this is better than statically modify. using js is easier. 
<img src="https://www.dropbox.com/s/b8k4wu2bryelj7l/Screenshot%202018-05-01%2002.22.41.png?raw=1" width="400">
again, note how you have to use string. 
<img src="https://www.dropbox.com/s/4ogcv20uc0uxmib/Screenshot%202018-05-01%2002.24.31.png?raw=1" width="400">

<img src="https://www.dropbox.com/s/g78aqcloml1emn7/Screenshot%202018-05-01%2002.26.48.png?raw=1" width="400">
remember again, `forEach` does not work for this return value list. 

also, note the results for this, some are relative paths, some are web paths. 

### lec158, 159
<img src="https://www.dropbox.com/s/hgsqjxrzaxb1l7k/Screenshot%202018-05-01%2002.29.01.png?raw=1" width="400">
<img src="https://www.dropbox.com/s/y4vjj99gbdcmlol/Screenshot%202018-05-01%2002.29.28.png?raw=1" width="400">
<img src="https://www.dropbox.com/s/tmfkr2lnzgrix7z/Screenshot%202018-05-01%2002.30.33.png?raw=1" width="400">
you can have multiple listeners to the same event on the same element. 
<img src="https://www.dropbox.com/s/6w2i9olggpok8m1/Screenshot%202018-05-01%2002.32.55.png?raw=1" width="400">
note that this click refers to the `ul`: it's the whole thing, so you click anywhere in the range of the `ul`, the even listener triggers. if you want to add listener to all `li`: 
<img src="https://www.dropbox.com/s/z49vk7cpvnfxgam/Screenshot%202018-05-01%2002.34.26.png?raw=1" width="400">
unfortunately a loop is unavoidable. 
<img src="https://www.dropbox.com/s/j13jj0qtqjcase4/Screenshot%202018-05-01%2002.35.18.png?raw=1" width="400">
note how `this` is used: which does it refer to here? it's a listener function, so it actually refers to the subject/owner of the listener. yes it's dynamic! when the function is evaled, `this` is resoluted dynamically, at the time of eval, to refer to the object that owns this listener.  
also, this is a very common pattern: select, loop, do something.  

[toggle.html](toggle.html) [toggle.js](toggle.js)

```html
<!DOCTYPE html>
<html>
<head>
    <title>Color Toggle</title>

    <style type="text/css">
    .purple {
        background: purple;
    }
    </style>

</head>
<body>
    <button>CLICK ME</button>


    <script type="text/javascript" src="toggle.js"></script>
</body>
</html>
```
note again, how `script` has to be the bottom, after `button` loaded. 

```js
var button = document.querySelector("button");
// var isPurple = false;


// button.addEventListener("click", function(){
//  if(isPurple){
//      document.body.style.background = "white";
//  } else {
//      document.body.style.background = "purple";
//  }
//  isPurple = !isPurple;
// });


button.addEventListener("click", function(){
    document.body.classList.toggle("purple");
});
```
note again how `document.body` is just some sugar: like querySelector ("body") or something.  
note how `toggle` here makes things so much easier. always think this way, rather than manually manipulate properties directly. `classList` is the usual way of doing things like this. 

```html
<!DOCTYPE html>
<html>
<head>
    <title>Score Keeper</title>
    <link rel="stylesheet" type="text/css" href="scorekeeper.css">
</head>
<body>

<h1><span id="p1Display">0</span> to <span id="p2Display">0</span></h1>

<p>Playing to: <span>5</span></p>

<input type="number">
<button id="p1">Player One</button>
<button id="p2">Player Two</button>
<button id="reset">Reset</button>

<script type="text/javascript" src="scorekeeper.js"></script>
</body>
</html>
```

```js
var p1Button = document.querySelector("#p1");
var p2Button = document.getElementById("p2");
var resetButton = document.getElementById("reset");
var p1Display = document.querySelector("#p1Display");
var p2Display = document.querySelector("#p2Display");
var numInput = document.querySelector("input");
var winningScoreDisplay = document.querySelector("p span");
var p1Score = 0;
var p2Score = 0;
var gameOver = false;
var winningScore = 5;

p1Button.addEventListener("click", function(){
    if(!gameOver){
        p1Score++;
        if(p1Score === winningScore){
            p1Display.classList.add("winner");
            gameOver = true;
        }
        p1Display.textContent = p1Score;
    }
});

p2Button.addEventListener("click", function(){
    if(!gameOver){
        p2Score++;
        if(p2Score === winningScore){
            p2Display.classList.add("winner");
            gameOver = true;
        }
        p2Display.textContent = p2Score;
    }
});

resetButton.addEventListener("click", function(){
    reset();
});

function reset(){
    p1Score = 0;
    p2Score = 0;
    p1Display.textContent = 0;
    p2Display.textContent = 0;
    p1Display.classList.remove("winner");
    p2Display.classList.remove("winner");
    gameOver = false;
}

numInput.addEventListener("change", function(){
    winningScoreDisplay.textContent = this.value;
    winningScore = Number(this.value);
    reset();
});
```

```css
.winner {
    color:green;
}
```

<img src="https://www.dropbox.com/s/oc3p28zmjcsq95g/Screenshot%202018-05-01%2002.45.23.png?raw=1" width="400">
notice how he uses this `alert` to do debugging. js这个界面交互真的是简单. 

```html
<h1><span id="p1Display">0</span> to <span id="p2Display">0</span></h1>
```
this is to separate regions in the same text content area: this is better than assembling the entire text content yourself by hand. 

这个例子如果你仔细看可以发现, 一个小小的页面背后实际上写一个逻辑也并不是那么简单的; 

### lec161, 

> Meanwhile, some students have been asking about the difference between the input and change event listeners, [here](https://stackoverflow.com/a/17047607/3176573)'s a good explanation of both - https://stackoverflow.com/a/17047607/3176573

<img src="https://www.dropbox.com/s/5fbzff0sfmfewmc/Screenshot%202018-05-01%2002.54.27.png?raw=1" width="400">
这个是他一直用的一个debug技巧, 每次select了一个东西之后, 立刻就直接写单独的一行, 然后`console.log`出来, 然后在浏览器里面看一下有没有结果; 这个其实跟平时print debug是差不多的;  
notice that:
```js
    p1Display.classList.remove("winner");
    p2Display.classList.remove("winner");
```
he does not really check which one is the winner, just do it for both: `remove` won't return error if the class does not exist in the class list.  

also, first time seen this:
```html
<input type="number">
```

<img src="https://www.dropbox.com/s/mf4yy199n0lr3l0/Screenshot%202018-05-01%2003.01.24.png?raw=1" width="400">

note how this `value` attribute is actually a string. 

fun bug:
<img src="https://www.dropbox.com/s/92vzrtg4kq88mfb/Screenshot%202018-05-01%2003.02.40.png?raw=1" width="400">
should be easy to see: you are comparing `5` to `"5"` with `===`. one way to fix would be to use `==`, but abuse of that is dangerous. the solution took another approach. 

this is the problem with untyped language:
<img src="https://www.dropbox.com/s/ler68envyrx4ktt/Screenshot%202018-05-01%2003.03.57.png?raw=1" width="400">
notice how here when you set the input, the var suddently is assigned to a string, which is previously a number. 

and also see why you have to refactor the `reset` function: it's used both when `reset` itself is clicked, and when the max score is changed. it's a reasonable design choice. 

<img src="https://www.dropbox.com/s/b4ppyojz2wn98g8/Screenshot%202018-05-01%2003.07.49.png?raw=1" width="400">
notice how he refactored this code to use `this`. 

### lec163
```html
<!DOCTYPE html>
<html>
<head>
    <title>Todo List Demo</title>
    <link rel="stylesheet" type="text/css" href="todos.css">
</head>
<body>

<ul>
    <li>Wash Cat</li>
    <li>Feed Cat</li>
    <li>Feed Cat to Dog</li>
</ul>

<script type="text/javascript" src="todos.js"></script>

</body>
</html>
```

```css
.done {
    text-decoration: line-through;
    opacity: 0.5;
}

.selected {
    color: green;
}
```
```js
var lis = document.querySelectorAll("li");

for(var i = 0; i < lis.length; i++){
    lis[i].addEventListener("mouseover", function(){
        this.classList.add("selected");
    });

    lis[i].addEventListener("mouseout", function(){
        this.classList.remove("selected");
    });

    lis[i].addEventListener("click", function(){
        this.classList.toggle("done");
    });
}
```

note:
```js
    lis[i].addEventListener("mouseover", function(){
        this.classList.add("selected");
    });
```
this is edge-triggered: so when you hover over it, it's not constantly firing. but this only takes care of the turn-on edge. add this to take care of the down-edge:
```js
    lis[i].addEventListener("mouseout", function(){
        this.classList.remove("selected");
    });
```
again, notice how we use class to manipulate properties instead of manually. this is especially useful in this case: you will need an *do* and an *undo* operation and class list just naturally handles that. also note how you constantly have to use `this` in the listener: it can also be seen like a pattern.  
one minor thing, even you did not define `selected`, this would still result in the class being added/removed from the class list. the language does not check for that.  
using class to manipulate css is also separation of concerns: css manages the styles, and js manages turning on or off parts of the css styles. 
<img src="https://www.dropbox.com/s/qql3q6njscpj3ee/Screenshot%202018-05-01%2013.42.15.png?raw=1" width="400">
test your results this way. you can see the item's class list changing dynamically as a response of your events. 

### lec164, 165, 166, 167
<img src="https://www.dropbox.com/s/73ag44xmqgl9w43/Screenshot%202018-05-01%2013.44.39.png?raw=1" width="400">
count the number of even entries listed in the page. this is just selecting elements and counting. experiment with console first. first, find out how many tables there are:
<img src="https://www.dropbox.com/s/m1eemsgtmamg4cs/Screenshot%202018-05-01%2013.45.16.png?raw=1" width="400">
and figure out which of these tables you want. now we are sure that we want all `tr`s in all `table`s, so do:
<img src="https://www.dropbox.com/s/u6k3rkuzrfx6qlb/Screenshot%202018-05-01%2013.46.02.png?raw=1" width="400">
we have to exclude the `tr` for table headers. 
<img src="https://www.dropbox.com/s/83v3a9o8wirjnkg/Screenshot%202018-05-01%2013.47.45.png?raw=1" width="400">

> If you complete the exercise, but your color choice shows "Wrong" even when it is correct, then take a look at your colors array and make sure that the colors have spaces after the commas in the RGB expression, otherwise the picked color will not match the randomly selected color.

这个空格就很烦人了; 

> e.g.,  
> Correct: "rgb(255, 0, 0)"  
>   
> Incorrect: "rgb(255,0,0)"  

this is fun: https://stackoverflow.com/questions/5657964/css-why-doesn-t-percentage-height-work/5658062#5658062

### lec168, 169, 170, 171
[colorGame.html](colorGame.html), [colorGame.css](colorGame.css), [colorGame.js](colorGame.js)

<img src="https://www.dropbox.com/s/mb2hxt6f2lhir1q/Screenshot%202018-05-01%2014.02.19.png?raw=1" width="400">
所以这里是介绍了这两个的区别, 这个也是我之前一直疑惑的一个东西: 看起来一样的效果不过老师一会儿用这个一会儿用那个;

井号“#”的术语是“octothorpe”. 
```js
                messageDisplay.textContent = "Correct!";
```
note this does not go against the use class list idiom: `textContent` is not the same as style properties, and direct manipulate is accepted;   
similarly random:
<img src="https://www.dropbox.com/s/m7bk4id6m5pfep3/Screenshot%202018-05-01%2014.17.23.png?raw=1" width="400">

```js
function randomColor(){
    //pick a "red" from 0 - 255
    var r = Math.floor(Math.random() * 256);
    //pick a "green" from  0 -255
    var g = Math.floor(Math.random() * 256);
    //pick a "blue" from  0 -255
    var b = Math.floor(Math.random() * 256);
    return "rgb(" + r + ", " + g + ", " + b + ")";
}
```
note how everything is string here with js. 
<img src="https://www.dropbox.com/s/ylz56vi0i0ft33o/Screenshot%202018-05-01%2014.28.19.png?raw=1" width="400">
这里好像就是之前为什么强调一定要有空格: 因为最后当我们set之后, DOM css自动就给这个`rgb`加了空格; 所以我们自己写的时候也要这样做, 因为我们有一个和他进行比较的过程:
```js
        squares[i].addEventListener("click", function(){
            //grab color of clicked square
            var clickedColor = this.style.background;
            //compare color to pickedColor
            if(clickedColor === pickedColor){
                messageDisplay.textContent = "Correct!";
                resetButton.textContent = "Play Again?"
                changeColors(clickedColor);
                h1.style.background = clickedColor;
            } else {
                this.style.background = "#232323";
                messageDisplay.textContent = "Try Again"
            }
        });
```
这里这个`this.style.background`返回来的自动就是有空格的版本, 所以你和他比较的时候要对应. 为了统一, 所以自己最后写这些string的时候, 就最好还是注意和这些标准进行统一对应. 

<img src="https://www.dropbox.com/s/77a73ggae7ixpu3/Screenshot%202018-05-01%2014.34.03.png?raw=1" width="400">
this won't set all text in the color to white, as you would expect: after all we are selecting an id already, how specific need be? 
<img src="https://www.dropbox.com/s/p2e6b8qllk0bhfm/Screenshot%202018-05-01%2014.34.52.png?raw=1" width="400">
this is because the id only gets you to the parent. but the `span` above actually targets the *message* directly, within the `span`, thus more specific. 

### lec172, 173
easy和hard两个按钮的状态互动, 他一开始用这个简单的做法: 
<img src="https://www.dropbox.com/s/adeu0t0v6ywurdk/Screenshot%202018-05-01%2014.51.21.png?raw=1" width="400">
这个也不错; 当然最后的逻辑实现是挺丑的: 
```js
function setupModeButtons(){
    for(var i = 0; i < modeButtons.length; i++){
        modeButtons[i].addEventListener("click", function(){
            modeButtons[0].classList.remove("selected");
            modeButtons[1].classList.remove("selected");
            this.classList.add("selected");
            this.textContent === "Easy" ? numSquares = 3: numSquares = 6;
            reset();
        });
    }
}
```
还需要对button的text进行一个比较; 太想要用generic的方式处理所有的button, 最后得到的代码反而有点不伦不类; 
<img src="https://www.dropbox.com/s/5q98v66exxx9e7j/Screenshot%202018-05-01%2014.55.44.png?raw=1" width="400">
use `display` property. 另外注意这里一个问题, 最后因为要区分两个mode, 如果是easy, 只要三个格子, 如果是hard, 就要6个格子. 他最后并没有在HTML上面对这两行进行区分, 而是还是整个当成一个长度为6的list在js里面拿到手, 然后自己循环处理的时候去区分. 这样的一个决定是不是最好的呢? 还不好说; 不过因为js本身自由度比较高, 他把这种各种各样的逻辑更加优先在js里面实现, 也是说得过去的; 

<img src="https://www.dropbox.com/s/463k20zi4un9924/Screenshot%202018-05-01%2015.09.29.png?raw=1" width="400">
the little black margin on the sides of `h1` is actually coming from the `body` (it does not get as closesly possible with the container: the window), rather than the `h1` itself: we already fixed that.  
```css
body {
    background-color: #232323;
    margin: 0;
    font-family: "Montserrat", "Avenir";
}
```
this provides two choices for the fonts, in case one of them fails. in that case, the fonts would fall back to the system defaults.  
note how this is to remove the default border of a button:
```
    border: none;
    background: none;
    font-size: inherit;
```
```css
button:hover {
    color: white;
    background: steelblue;
}
```
maybe this can also be done in js? but since it's quite pre-defined behavior, changing it in css itself might make sense. 
```
    transition: all 0.3s;
```
this means, whenever any properties *changes*, take 0.3 second. the prooperties in the case of the button for instance, is the `background` and the `color`. note that this does not do things that listens to event like `:hover`, but rather, this applies to changes that are *already* caused by things like `:hover`.  
```
    transition: background 0.6s;
```
see here, it specifies a particular property `background` to apply the transition to. 
```
    -webkit-transition: background 0.6s;
    -moz-transition: background 0.6s;
```
this is for browser compatibility, nothing different in functionality. `transition` property is not built in to all browsers. 

### lec174, 175
get rid of this:
<img src="https://www.dropbox.com/s/4w5fdcnsvjpdx1p/Screenshot%202018-05-01%2015.25.38.png?raw=1" width="400">
this is what the browser did automatically. 
```
    font-weight: normal;
```
this does it.  
```js
    for(var i = 0; i < modeButtons.length; i++){
        modeButtons[i].addEventListener("click", function(){
            modeButtons[0].classList.remove("selected");
            modeButtons[1].classList.remove("selected");
            this.classList.add("selected");
            this.textContent === "Easy" ? numSquares = 3: numSquares = 6;
            reset();
        });
    }
```
note how he did this again: unconditionally reset any, then choose the one I want, then *set* that only. 这个反正是一个个人选择上的风格;  
```js
    for(var i = 0; i < squares.length; i++){
        if(colors[i]){
            squares[i].style.display = "block"
            squares[i].style.background = colors[i];
        } else {
            squares[i].style.display = "none";
        }
    }
```
note here how uses the `colors[i]` to control what to do with `display`. this is not bad: mode defines the number of colors, then that defines each entry in `colors`, then use that to control the `display` property of each `squares[i]`.  
why would that happen, because in the beginning of `reset`, we get the `colors` in this way:
```js
    colors = generateRandomColors(numSquares);
```
this only returns an array of 3 in easy mode, and when you access something like `colors[4]` which is out of bound, you get `undefined`:
```js
!!null
false
!!undefined
false
var ar = [1,2,3]
undefined
ar[4]
undefined
```
这里老师上课的时候认为这里最后得到的是`null`, 实际上是错误的, 出界给的是`undefined`.  

### lec176, 177, 178, 179, 180, 181
jquery helps us manipulate the DOM. it's a js lib. used to manipulate css, ajax etc. just makes some things we already can do easier with DOM. everything you can do with jquery, you can do without: http://youmightnotneedjquery.com

it's been an active debate. 
<img src="https://www.dropbox.com/s/ggwt1paa4qic7ca/Screenshot%202018-05-01%2015.49.16.png?raw=1" width="400">
<img src="https://www.dropbox.com/s/pjt0gdliw0sm53h/Screenshot%202018-05-01%2015.50.21.png?raw=1" width="400">

the course uses 2.1.4 jquery version. 

[jqueryDemo.html](jqueryDemo.html), 

<img src="https://www.dropbox.com/s/ph90zbie1ey51kg/Screenshot%202018-05-01%2015.59.48.png?raw=1" width="400">

also you can install with CDN.  

<img src="https://www.dropbox.com/s/ihv04st44az42l3/Screenshot%202018-05-01%2016.01.19.png?raw=1" width="400">

<img src="https://www.dropbox.com/s/6m5b9cvzrd93nt5/Screenshot%202018-05-01%2016.02.38.png?raw=1" width="400">
<img src="https://www.dropbox.com/s/7wl6js4z2k3eqhc/Screenshot%202018-05-01%2016.03.04.png?raw=1" width="400">
<img src="https://www.dropbox.com/s/ggz06cxx4p2tt1z/Screenshot%202018-05-01%2016.06.12.png?raw=1" width="400">
<img src="https://www.dropbox.com/s/acwgzwkt3pivc8y/Screenshot%202018-05-01%2016.06.37.png?raw=1" width="400">
still, all strings, because it's still js code. but wait , jquery can also take an object as above shown. although actual values for each property should still be strings. yes, js does not provide something like `document.body.style = some object`. 
<img src="https://www.dropbox.com/s/eez136hlt22f2ol/Screenshot%202018-05-01%2016.08.46.png?raw=1" width="400">
another limitation of js is, you can only manipulate one element a time: remember how we have to use loop everywhere. this is much easier in jquery.  
reminder: in js and jquery:
<img src="https://www.dropbox.com/s/gcvvohu72rk3clq/Screenshot%202018-05-01%2016.10.53.png?raw=1" width="300">
property names has to be camel case rather than with dash lines `-`. 

[exercise.html](exercise.html), [exercise.js](exercise.js); 
```html
<!DOCTYPE html>
<html>
<head>
    <title>jQuery Exercise</title>
    <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.1.4/jquery.min.js"></script>
</head>
<body>
    <div>Div 1</div>
    <div class="highlight">Div 2</div>
    <div id="third">Div 3</div>
    <div class="highlight">Div 4</div>

    <script type="text/javascript" src="exercise.js"></script>
</body>
</html>
```
note how you have to include the `script` twice; they have different `src` and serve different purposes. the reason is this, first in `head`, we load jquery, so we can use it in our code. also, the second `script` is late, because we want the static html to load before we run the script.  
check that your jquery works:
<img src="https://www.dropbox.com/s/0eaireitdbm1gu8/Screenshot%202018-05-01%2016.18.46.png?raw=1" width="400">
```js
// Select the divs with class "highlight" and make them 200px wide
$("div.highlight").css("width", "200px");
```
this means all `div`s with class `hightlight`: note the similarity and different compared with `.hightlight` used alone. 
```js
// Bonus: Select the first div only and change its font color to pin
$("div:first-of-type").css("color", "pink");
```
this pseudo-selector is new.  
<img src="https://www.dropbox.com/s/gwgycn1kdusy4z6/Screenshot%202018-05-01%2016.21.44.png?raw=1" width="400">
this also work, which is a shortcut built-in in jQuery. but this is actually slower, because it's not *native* to css.  

### lec182, 183, 184
common methods:
<img src="https://www.dropbox.com/s/3piv092ne2e29uf/Screenshot%202018-05-01%2016.22.37.png?raw=1" width="400">
<img src="https://www.dropbox.com/s/wvm77bx951wtq07/Screenshot%202018-05-01%2016.25.54.png?raw=1" width="400">
notice how when you are selecting all `li`, the final content is concatenated together.  the above uses 0arg, you can pass in arguments: 
<img src="https://www.dropbox.com/s/5lmlu4lfeoqufmv/Screenshot%202018-05-01%2016.26.36.png?raw=1" width="400">
then it just acts like a `set` method instead of a `get`. but it might not always be what you want:
<img src="https://www.dropbox.com/s/lxtkkmaa3sm8v0d/Screenshot%202018-05-01%2016.27.38.png?raw=1" width="400">
notice how the one string is broadcast to all `li`. this can be problematic. vanilla js would allow more flexibility. 

`html` just like `innerHTML`. some quirks:
<img src="https://www.dropbox.com/s/cbwran4k87sfyh2/Screenshot%202018-05-01%2016.28.44.png?raw=1" width="400">
`get` only returns the first, while `set` actually sets all in the list. again, `text` can't do the same thing: it's html-safe, meaning html tags in it won't be interpreted/rendered.  

<img src="https://www.dropbox.com/s/qxh7ydretyd3q2w/Screenshot%202018-05-01%2016.32.41.png?raw=1" width="600">
how about delete attribute? again, notice how attribute is different from property. 
* attribute: things like `src` of `a` in html; 
* property: things like `margin-top` in css; 

they both act on html elements though. 
<img src="https://www.dropbox.com/s/lwny3rj7a8izvui/Screenshot%202018-05-01%2016.35.41.png?raw=1" width="400">
changing the `type` of `input` can be powerful.  
of course, jQuery can still work around the broadcasting behavior: 
<img src="https://www.dropbox.com/s/e4qw9hgbvph97xl/Screenshot%202018-05-01%2016.37.00.png?raw=1" width="400">
it just requires a little css trick now. now you don't do those intra-list logic in js, but rather with css.  what about last?
<img src="https://www.dropbox.com/s/uzkv3hvonfow40o/Screenshot%202018-05-01%2016.38.07.png?raw=1" width="400">
seems a lot of api to remember. `nth-of-type` should be convenient. but what about range query? not sure how to do so far. 
<img src="https://www.dropbox.com/s/ra4rrj2qrq504ug/Screenshot%202018-05-01%2016.40.05.png?raw=1" width="400">
`select.foo` means the `select` **elemenet** with **class** `foo`. 不要用传统编程里面的dot来理解; `select`本身什么前缀都没有, 所以就是一个tag而已; 

<img src="https://www.dropbox.com/s/wt6jj2bxj3k2m07/Screenshot%202018-05-01%2016.45.11.png?raw=1" width="400">
notice how the last one clears the input box. last thing, `.val()` actually works on all elements with `value` attribute, so not just `input`. like drop down menus, which is `select` element. 这么看来`attr`和`val`是不是有点重叠啊? `value`本身也是一个attribute. 

<img src="https://www.dropbox.com/s/aahfjzhn4yb3hrw/Screenshot%202018-05-01%2016.51.16.png?raw=1" width="400">
注意看这里, 实际上还是有区别的; `attr`本身实际上就是在element的定义本身里面去找这个attribute: 如果HTML里面没有写`value`这个attribute, 那么`attr`就没有办法把它给提取出来; 但是对于这里这个例子
```html
    <input type="text" name="">
```
实际上直接用`val`照样可以用, 即使根本没有explicit的写出来`value`这个attribute; 

<img src="https://www.dropbox.com/s/6idsnquwedfcnek/Screenshot%202018-05-01%2016.53.57.png?raw=1" width="400">
<img src="https://www.dropbox.com/s/p6tqsy3015yrkwd/Screenshot%202018-05-01%2016.54.33.png?raw=1" width="400">
note that broadcast also applies. 
<img src="https://www.dropbox.com/s/14pj996spqs5dbj/Screenshot%202018-05-01%2016.55.37.png?raw=1" width="400">
<img src="https://www.dropbox.com/s/xs9zr8bz0uwmzx0/Screenshot%202018-05-01%2016.55.52.png?raw=1" width="400">
notice how `first` is also available. 


















































