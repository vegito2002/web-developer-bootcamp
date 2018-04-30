### lec85,86 js console
js is the *verb*. 
<img src="https://www.dropbox.com/s/cafmvqcr56a13l8/Screenshot%202018-04-30%2015.47.29.png?raw=1" width="400">
not usually used often. just some in place interaction or debugging. just like how you can change the css in place, you can change the js behavior in place too. 

### lec87,88,89,90,91,92
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

