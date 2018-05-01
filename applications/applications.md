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

<img src="https://www.dropbox.com/s/7rjvvtktv0w0yco/Screenshot%202018-05-01%2001.20.52.png?dl=0" width="400">
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




































