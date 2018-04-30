### lec13
HTML is the noun, CSS is the adjective, JavaScript is the verb.  

![](https://www.dropbox.com/s/1s6wc12a4bb63q8/Screenshot%202018-04-02%2001.04.32.png?raw=1)

### lec15
boilerplate: 打一下html然后tab就行了; 
```html
<!DOCTYPE html>
<html>
<head>
<!-- Our metadata goes here -->
  <title></title>
</head>
<body>

<!-- Our content goes here -->

</body>
</html>
```

### lec17
find help:
![](https://www.dropbox.com/s/mf0r9h0xj181wem/Screenshot%202018-04-02%2001.16.59.png?raw=1)

### lec18
```html
<h1>I need a closing tag </h1>

<p>Me too!</p>

<!-- No closing tag or inner text needed -->

<img src="corgi.png">

<link href="style.css">

<!-- Don't worry about what these tags do yet -->
```

type html and then tab. You have the boilerplate in ST.

These are all titles:
![](https://www.dropbox.com/s/ncecexlxfbfp2fy/Screenshot%202018-04-02%2002.33.18.png?raw=1)

`h1` are block-level: each gets their own line automatically. Even if you don't add newline.  
Others are called inline elements.  
so is `p`, also block-level.   
wrap tag shortcut: ctrl+shift+w  
so `b` is also inline, it still won't force things down to a new line.  
`strong` is more preferable than `b`. There is some difference. Also, `em` is bettern than `i`. This is seperating styling from structuring. Enforced in HTML5.  

### lec20
You can also tab-complete `li`.

### lec22
Exercise solution
```html
<!DOCTYPE html>
<html>
<head>
    <title>Things I've Learned</title>
</head>
<body>

<h1>Things I've Learned</h1>

<h2>Internet Basics</h2>

<ol>
    <li>HTTP Requests</li>
    <li>IP Address</li>
    <li>Servers</li>
</ol>

<h2>HTML</h2>

<ul>
    <li>Stands for <strong>Hyper Text Markup Language</strong></li>
    <li>Lots of Tags
     <ul>
        <li>Boilerplate
          <ol>
            <li>Doctype</li>
            <li>HTML</li>
            <li>Head
                <ol>
                    <li>Title</li>
                </ol>
            </li>
            <li>Body</li>
          </ol>
        </li>
        <li>Headings</li>
        <li>Paragraph</li>
        <li><em>em</em></li>
        <li><strong>strong</strong></li>
     </ul>
    </li>
</ul>

</body>
</html>
```

cmd+shift+d: duplicate line  
写这种nested的list的时候, 还是从最高层开始写, 然后慢慢深入, 找你想要展开继续nest的item, 然后继续写;   

### lec26
solutuion:
```html
<!DOCTYPE html>
<html>
<head>
    <title>Rusty Steele</title>
</head>
<body>

<h1>Rusty Steele</h1>
<p>Hi, I'm a dog.  Woof!</p>

<img src="http://i.imgur.com/Zl0A6erm.jpg">

<h3>Some of my favorite places:</h3>

<ul>
    <li>The beach</li>
    <li>The dog park</li>
    <li>The fire hydrant</li>
</ul>

<p>Make sure to follow me on <a href="https://instagram.com/dogsofinstagram/?hl=en">Instagram</a></p>
</body>
</html>
```

no close tag for `img`.  

### lec28
comment can't be nested either in html. 

```html
<table border="1">
    <thead>
        <tr>
            <th>Name</th>
            <th>Age</th>
            <th>Breed</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Rusty</td>
            <td>2</td>
            <td>Mutt</td>
        </tr>
        <tr>
            <td>Wyatt</td>
            <td>13</td>
            <td>Golden</td>
        </tr>
    </tbody>
</table>
```

### lec30
solution:
```html
<!DOCTYPE html>
<html>
<head>
    <title>Pokemon Chart</title>
</head>
<body>
<h1>First Gen Pokemon Chart</h1>

<table border="1">
    <thead>
        <tr>
            <th>Image</th>
            <th>Name</th>
            <th>Type</th>
            <th>Evolves Into</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><img src="http://img4.wikia.nocookie.net/__cb20140328190757/pokemon/images/thumb/2/21/001Bulbasaur.png/200px-001Bulbasaur.png"></td>
            <td>Bulbasaur</td>
            <td>Grass/Poison</td>
            <td><a href="http://pokemon.wikia.com/wiki/Ivysaur">Ivysaur</a></td>
        </tr>
        <tr>
            <td><img src="http://img4.wikia.nocookie.net/__cb20140724195345/pokemon/images/thumb/7/73/004Charmander.png/200px-004Charmander.png"></td>
            <td>Charmander</td>
            <td>Fire</td>
            <td><a href="http://pokemon.wikia.com/wiki/Charmeleon">Charmeleon</a></td>

        </tr>
        <tr>
            <td><img src="http://img1.wikia.nocookie.net/__cb20140328191525/pokemon/images/thumb/3/39/007Squirtle.png/200px-007Squirtle.png"></td>
            <td>Squirtle</td>
            <td>Water</td>
            <td><a href="http://pokemon.wikia.com/wiki/Wartortle">Wartortle</a></td>
        </tr>
        
    </tbody>

</table>

</body>
</html>
```

`thead` and `tbody` doesn't really change any of the look.  
Usually styling is better done with CSS. CSS can even do scaling.  
这个练习最好的办法肯定是干脆直接写一个脚本来搞一下就行了.  

### lec31
One submit button for multiple input fields grouped together.  

### lec32
这一节做的这个forum页面在chrome里面用起来正常, 但是safari上面color那个按钮不行, 不知道为什么;

```html
<!DOCTYPE html>
<html>
<head>
    <title>Forum Demo</title>
</head>
<body>

<input type="text" name="">
<input type="color" name="">
<input type="radio" name="">
<input type="password" name="">

</body>
</html>
```

both identical:
```html
<button>Submit</button>
<input type="submit" name="">
```

default text:
```html
<input type="text" name="" placeholder="username">
<input type="password" name="" placeholder="password">
```

### lec33
form is also block-level:
```html
<form>
    <input type="text" name="" placeholder="username">
    <input type="password" name="" placeholder="password">
    <input type="submit" name="">
</form>

111
```

111 would be in the same line with the form without the form tag.

for the form as is:
```html
<!-- action - where the form send data to -->
<!-- method - what HTTP method (get/post) -->

<h1>Login</h1>
<form>
    <input type="text" name="" placeholder="username">
    <input type="password" name="" placeholder="password">
    <input type="submit" name="">
</form>
```

there is no action set for submit, so the default is just to send to where I am right now: fill in the form and submit, you will see the page refresh itself (refresh button clicked automatically).

The default method in this case is GET;

let's specify:
```html
<form action="http://wikipedia.org" method="GET">
    <input type="text" name="" placeholder="username">
    <input type="password" name="" placeholder="password">
    <input type="submit" name="">
</form>
```

so although it's called action, it's really the target. 

Usually we send that to our own backend. 

change the name:
```html
<form>
    <input type="text" name="username" placeholder="username">
    <input type="password" name="password" placeholder="password">
    <input type="submit" name="">
</form>
```

and after you submit, you see the URL: `file:///Users/vegito2002/Git/web-developer-bootcamp/notes/forms.html?username=1&password=2`; This format is query-string. `?` followed by `key=value` pairs separaetd by `&`. You see the data you filled in is being sent now. This makes retrieving the data easier later. Of course, this is not how psw really is sent. Usually that hiding can be done with a POST request instead of GET. 

Point is, when you fill in form and submit, the data you filled in is sent somewhere as a request. 

change action back to wiki, you again get `https://www.wikipedia.org/?username=1&password=2`. Data is added again. 

Extract data, send the data as query-string to backend. That's the point of a form.

### lec34
label makes the form itself more readable. It can also be used by certain software to extract the form information: auto read software. 

```html
<form>
    <label>
        Username: 
        <input type="text" name="username" placeholder="username">
    </label>
    <label>
        Password:
        <input type="password" name="password" placeholder="password">
    </label>
    
    <input type="submit" name="">
</form>
```

Rather than nest input inside label, we can make them separately. 
```html
<form>
    <label for="username">Username:</label>
    <input id="username" type="text" name="username" placeholder="username">

    <label for="password">Password:</label>
    <input id="password" type="password" name="password" placeholder="password">
    
    <input type="submit" name="">
</form>
```

for of label should match id of input: that's all required. 

### lec35
html itself offers some form validation. Usually that is done in js or java, but minimal support is also provided by html itself. we can check not_empty. 
```html
    <input id="username" type="text" name="username" placeholder="username" required>
```
this is actually browser specific: not all browser supports this. 

data type validation (format): email looks like an email. 

```html
    <label for="username">Email:</label>
    <input id="username" type="email" name="email" placeholder="username" required>
```
这个检查是很简单的, 比如email这里, type设置了之后, 就是只检查有一个@, 然后前后有东西就行了, 比如1@2这种他也认可的; 

### lec36
```html
<input type="radio" name="">
<input type="checkbox" name="">
```

```html
<input type="radio" name="">
<input type="radio" name="">
```
this is not exclusive. bad; this is done with `name`. for now, we know that `name` is used when sending data in the HTTP request. 

same `name` connects two `input`s. 
```html
<form>
    <label for="dogs">Dots: </label>
    <input id="dogs" name="pet_choice" type="radio" name="">

    <label for="cats">Cats: </label>
    <input id="cats" name="pet_choice" type="radio" name="">

    <button>Go!</button>
</form>
```
Note that if the last item in the `form` is a `button`, then clicking the button naturally submits the form. this results in `file:///Users/vegito2002/Git/web-developer-bootcamp/notes/inputs.html?pet_choice=on`. we see `pet_choice` is in a key-value pair, but the value is not right. Now you have `file:///Users/vegito2002/Git/web-developer-bootcamp/notes/inputs.html?pet_choice=CATS`. 
```html
<form>
    <label for="dogs">Dots: </label>
    <input id="dogs" name="pet_choice" type="radio" name="" value="DOGS">

    <label for="cats">Cats: </label>
    <input id="cats" name="pet_choice" type="radio" name="" value="CATS">

    <button>Go!</button>
</form>
```

```html
<form>
    <label for="dogs">Dots: </label>
    <input id="dogs" name="pet_choice" type="radio" name="" value="DOGS">

    <label for="cats">Cats: </label>
    <input id="cats" name="pet_choice" type="radio" name="" value="CATS">

    <p>Favorite Color?</p>
    <select>
        <option>Red</option>
        <option>Orange</option>
        <option>Yellow</option>
    </select>

    <button>Go!</button>
</form>
```
`file:///Users/vegito2002/Git/web-developer-bootcamp/notes/inputs.html?`. Nothing is submitted. Because we did not give `name`, so there is no way to add that as name-value pairs in the query-string. 

```html
    <select name="color">
        <option>Red</option>
        <option>Orange</option>
        <option>Yellow</option>
    </select>
```
`file:///Users/vegito2002/Git/web-developer-bootcamp/notes/inputs.html?color=Red`. The `value` is auto detected as the displayed text. what if we don't want that? 

```html
    <select name="mood">
        <option>:)</option>
        <option>:|</option>
        <option>:(</option>
    </select>
```
sends: `file:///Users/vegito2002/Git/web-developer-bootcamp/notes/inputs.html?mood=%3A%29`. This is weird. Then we specify `value`. 

```html
    <select name="mood">
        <option value="happy">:)</option>
        <option value="neutral">:|</option>
        <option value="sad">:(</option>
    </select>
```
`file:///Users/vegito2002/Git/web-developer-bootcamp/notes/inputs.html?mood=happy`. 

```html
    <input type="text" name="">
```
only works for a single line. That might not be enough. 
```html
    <textarea rows="10" cols="50"></textarea>
```

```html
    <textarea name="paragraph" rows="10" cols="10"></textarea>
```
: `file:///Users/vegito2002/Git/web-developer-bootcamp/notes/inputs.html?mood=happy&paragraph=paragraphcontent`

### lec37
![](https://www.dropbox.com/s/kbnp3pmgqdcr460/Screenshot%202018-04-29%2014.45.14.png?raw=1)
这个自己做了一下, 还是复习了不少东西的; 在[ForumSolution.html](ForumSolution.html). 

extra credit: password length 5-10 validation. you can use `minlength` and `maxlength` attribute, but this has less powerful browser support compared to pattern. 

这题的换行我是这样做的: 
```html
    <br>
    <label for="email">Email: </label>
    <input id="email" type="email" name="email" placeholder="your email" required>
    <label for="psw">Password: </label>
    <input id="psw" type="password" name="password" placeholder="your password" required>
```

老师的做法: 
```html
    <div>
        <label for="email">Email: </label>
        <input id="email" type="email" name="email" placeholder="your email" required>
        <label for="psw">Password: </label>
        <input id="psw" type="password" name="password" placeholder="your password" required>
    </div>
```
用`p`也行; 

```html
    <label>Birthday: 
        <select name="month">
            <option value="null">Month</option>
            <option value="jan">Jan</option>
            <option value="feb">Feb</option>
            <option value="mar">March</option>
        </select>
        <select name="day">
            <option value="null">Day</option>
            <option value="1">1</option>
            <option value="2">2</option>
            <option value="3">3</option>
        </select>
        <select name="year">
            <option value="null">Year</option>
            <option value="2016">2016</option>
            <option value="2017">2017</option>
        </select>
    </label>
```

这里的label用nesting比较好一点: 不然一个一个的写`for`和`id`太麻烦了: 这里一个`label`照顾的东西太多了;  另外注意上面默认值的写法; value可以用一个自己认识的特殊值来表示这个dropdown的value实际上是缺失的; 

```html
    <label for="aggred">I agree to the terms and conditions </label>
    <input id="agreed" type="checkbox" name="agree">
```
老师认为这里的label要跟这个checkbox连接起来, 我不知道为什么; 

最后长度validation他是在StackOverflow上面搜的一个用regex做的解法; 
```html
    <input id="psw" type="password" name="password" pattern=".{5,10}" required title="5 to 10 characters" placeholder="your password">
```
注意这里的5和10之间的逗号不能有空格; 好像HTML里面很多时候空格确实是不能乱加的; `title`基本就是error message. 老师的答案在[ForumSolution_teacher.html](ForumSolution_teacher.html).


## lec41
the adjective. separate documents, not in the html. we include them in html.   
good site: [http://www.csszengarden.com](http://www.csszengarden.com)
the site uses [css-zen-example.html](css-zen-example.html), and write their own css, without changing the html AT ALL.  
this site showcases what you can do, with JUST css.  

general rule
![](https://www.dropbox.com/s/d1dle0wpcatakwc/Screenshot%202018-04-29%2015.31.38.png?raw=1)
key-value format on each line; or property-value. select something, e.g. `h1`, they apply all property-value pairs to them, e.g. `color: purple`. There are much freedom, but this is the general format that always applies. 

### lec42
the file [aboutMe.html](aboutMe.html)

where to put the css? many choices. the old way: inline:
```html
    <li style="color: purple;">Playing Guitar</li>
```
this is not recommended. problem is if I want all three `li`, then a lot duplication is needed. another reason is we should separate css and html: separation of concerns. the other way: style tag. 
```html
<head>
    <title>About me</title>
    <style type="text/css">
        h1 {
            color: purple;
        }
    </style>
</head>
```
`li` selector selects *all* `li`s. if multiple selector for the same element, say `h1`, this is when there is conflicting. The one came later won. 

there is still problem: css still in html, not good. css should not be nested in html. use the `link` tag. separate css file, connect. need to be in the same directory. 

```html
    <link rel="stylesheet" type="text/css" href="aboutMe.css">
```
`href` refers where to find the file. 

the inline solution can use sometimes for demonstration or debugging: quick trick. do remember everything is in `head` scope. 

### lec44
more complicated colors, more customized.  

<img src="https://www.dropbox.com/s/q5t2lzezcn5fhia/Screenshot%202018-04-29%2015.48.17.png?raw=1" width="400">

the built-in color can be rich though. [http://colours.neilorangepeel.com](http://colours.neilorangepeel.com) is a good site to see the coloe is like. problem is the names are hard to remember. 

```css
h1 {
    color: #00FF00;
}
```
this is hexadecimal color. RGB each 2 digits. the above says Green all the way up, and no red and no blue. each color has 8bits, that is 0-255. FFFFFF is actually white: just like sunlight. a lot utilities called *colorpicker* are available on machine or online. [https://www.webpagefx.com/web-design/color-picker/](https://www.webpagefx.com/web-design/color-picker/) this is good. 

another way:
```css
h4 {
    color: rgb(0, 255, 0);
}
```
con't add space between left parens! other wise does not work. 
```css
li {
    color: rgba(111, 99, 150, 0.5);
}
```
make color transparent. additional 4th channel. `0..1`. A for alpha. 

### lec45
`background` property. 
```css
h1 {
    color: #FF8000;
    background: #3498db;
}
```
change the background to an image. 
```css
body {
    background: url(https://images.pexels.com/photos/259915/pexels-photo-259915.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940);
}
```

Sometimes when the image is small, there will be tiling (repeated stacking). turn that off. 
```
    background-repeat: no-repeat;
```
and to stretch the image:
```
    background-size: cover;
```
it is really your responsibility to make sure that the image is good enough. 

borders: width, color, style; three parts. 

```
h1 {
    color: rgba(0, 200, 100, 0.8);
    border-color: purple;
    border-width: 5px;
    border-style: solid;
}
```
the border won't be visible unless all three parts are present. usually a shortcut syntax: 
```css
h1 {
    color: rgba(0, 200, 100, 0.8);
    border: 5px solid purple;
}
```

### lec47
```html
    <link rel="stylesheet" type="text/css" href="todo.css">
```
add this before adding the css file: error-driven development. create file, add something like this:
```css
body {
    background: orange;
}
```
to make sure that the linking is working. this is the main scenario you explicitly use built-in color. we can select all `li`. how to single one out. we have to modify the html to add a hook for the css to refer to it. `id` here we use. it's an attribute to any element, and any name you want. then later refer to that later with `#id` something like this. 
```css
#special {
    color: green;
}
```
on a single page, the id values can't conflict.   
but what if we want to specify a subgroup, not just an individual? use `class`. it's just like `id`, except it can be any number. `id` like person name, `class` like company name or team name.  
```html
<ul>
    <li class="completed">
        <input type="checkbox" name="">
        Walk Rusty
    </li>
    <li class="completed">
        <input type="checkbox" name="">
        Buy Groceries
    </li>
    <li id="special">
        <input type="checkbox" name="">
        Finish Videos
    </li>
</ul>
```
note that `class` and `id` are all added to `li` rather than `input`. 
then select:
```css
.completed {
    text-decoration: line-through;
}
```
btw, if you want the checkbox to be checked by default:
```html
    <li class="completed">
        <input type="checkbox" name="" checked>
        Walk Rusty
    </li>
```

### lec48
chrome html/css developer tools. view page source. inspect element. this is even better. 
<img src="https://www.dropbox.com/s/1ff5vsfu7ni3x75/Screenshot%202018-04-29%2016.32.24.png?raw=1" width="400">

click on `li`, then you can see on the right all styles applied. you can even turn them on an off with toggle. or directly edit e.g. `border`. this does not change the file though, it's all only in the browser. this is very good for debugging. also good when you see a website and want to know maybe what color/font they are using. 点放大镜, 然后在页面上面点, 就可以直接选中这个element, 然后inspect; 

### lec49
[Good selectors](https://code.tutsplus.com/tutorials/the-30-css-selectors-you-must-memorize--net-16048) to know about. 

[07.html](07.html). 
```css
/*Star*/
* {
    border: 1px solid lightgrey;
}
```
everything. not really useful often.
```css
/*Descendant Selector*/
li a {
    color: red;
}
```
very useful. I want all `a` that are descendants of `li`. writing `ul li a` can also work but no different in this case. 
```css
/*Adjacent Selector*/
h4 + ul {
    border: 4px solid red;
}
```
not nesting, but that *comes after*, a sibling. directly a sibling, on the same level.  
```css
/*Attribute Selector*/
a[href="http://www.google.com"] {
    background: blue;
}
```
```css
input[type="text"] {
    background: orange;
}
```
just is `a` with some more filter based on attributes. same to do with all `input` with some `type` etc. 
```css
/*nth of type*/
li:nth-of-type(odd){
    background: purple;
}
ul:nth-of-type(3) {
    background: pink;
}
```
`odd` is special, you can also use just numbers. 1-based. 
```css
li:nth-of-type(3) {
    background: pink;
}
```
this will only select the 3rd `li` in each `ul`. why delimited by `ul`? that's the group concept here. 

### lec50
[specificity.html](specificity.html). changing the `color` of an `ul` makes all `li` inside inherit that color. also like `body` can change everything on the page. so you don't have to explicitly select everything within. Just one that includes all. 
```css
    body {
        color: red;
    }

    p {
        color: green;
    }
```
use later smaller scope to override. multiple rules apply to the same element. 
<img src="https://www.dropbox.com/s/5jvhzh4wmixhlm4/Screenshot%202018-04-29%2016.58.29.png?raw=1" width="400">

see the cross out of the one inherited. specificity is related to inheritance. one element is being targeted by many rules. whichever rule that is more specific is going to win. but this is simple case. 
```html
<!DOCTYPE html>
<html>
<head>
    <title>Specificity</title>
    <style type="text/css">
    body {
        color: red;
    }
    ul {
        color: blue;
    }
    li {
        color: orange
    }
    .highlight {
        color: yellow;
    }
    </style>
</head>
<body>

<p>HELLO</p>

<ul>
    <li class="highlight">John</li>
    <li class="highlight">Paul</li>
    <li>George</li>
    <li>Ringo</li>
</ul>

</body>
</html>
```
in this case, the `highlight` class wins. degree of being specific does not resolve this. some precedence rules. likewise, `id` can win `class`. [an online calculator](https://specificity.keegan.st) to demonstrate how the numerical calulation is done for resolving the precedence. basically, tag not so specific, class more, id is the most specific. `.class1 .class2`, this is only 20 (this is class inside class), but `#id1` is much more specific, 100 like. these are selectors you use in css, and their precedence is calculated this way.   
attribute selector is also very specific. Pseudo-Class also specific:
```
a:hovered
```
这个不知道是什么. 


### lec52
[selectorsExercise.html](selectorsExercise.html). [solution](selectorsExercise.css)
some complicated:
```css
/* Give the 2nd <p> inside the 3rd <div> a 5px white border*/
div:nth-of-type(3) p:nth-of-type(2){
    border: 5px solid white;
}
```
extra credits:
```css
/*BONUS CHALLENGES*/
/*You may need to research some other selectors and properties*/

/*Make all "checked" checkboxes have a left margin of 50px(margin-left: 50px)*/
input:checked{
/* add space on left: to move it */
    margin-left: 50px;
}
/* Make the <label> elements all UPPERCASE without changing the HTML(definitely look this one up*/
label {
    text-transform: uppercase;
}

/*Make the first letter of the element with id 'special' green and 100px font size(font-size: 100)*/
#special:first-letter {
    color: green;
    font-size: 100px;
}

/*Make the <h1> element's color change to blue when hovered over */
h1:hover {
    color: blue;
}

/*Make the <a> element's that have been visited gray */
a:visited {
    color:gray;
}
```
note that this:
```css
input:checked{
    margin-left: 50px;
}
```
will actually also select all radio buttons. we don't have any here but do remember checkboxes are not the only thing that can be checked. 

### lec55
[fonts.html](fonts.html), [fonts.css](fonts.css). ipsum generator. generate pointless text that are at least text. [this one](https://baconipsum.com) is funny. different machine and different browser has different sets of fonts available. look at: https://www.cssfontstack.com. usually using custom fonts is better: later about that.  
```css
p {
    font-family: Arial; 
}
```
you can put quotes, and you have to if the font has number in the beginning. does not matter here. 
```css
/* font-size */
h1 {
    font-size: 100px;
}
```
set a number, then inspect and change in browser to find the best value you want.   
use `span` to group text, to single them out for operation. 
```css
span {
    font-size: 2.0em;
}
```
this means to make the texts in `span` to be double the size of the **enclosing element**. this is dynamic, and very useful. since it always refers to the parent, then what is the base case? it really depends on the browser. usually it's around 16px. usually people set the body font-size early in the css. 

### lec56
font weight: how thick the lines are. some fonts allows to use numbers in the range 100..800 (multiples of 100 only) to specify. but not all fonts works.  
`line-height` depends on the font itself.  
`text-decoration` does underline, strikethrough things. 

### lec58
[instructions](https://www.udemy.com/the-web-developer-bootcamp/learn/v4/t/lecture/6674650?start=0) on how to get the google fonts. one example: 
```html
<link href="https://fonts.googleapis.com/css?family=Open+Sans:400,600" rel="stylesheet">
```
built-in fonts are limitted and unreliable (can be unavailable).  
link to your own font file the same way.  

### lec59
<img src="https://www.dropbox.com/s/gqxrscl4gmm8cd2/Screenshot%202018-04-29%2019.10.24.png?raw=1" width="500">

remember these terminologies. 

[boxmodel.html](boxmodel.html), [boxmodel.css](boxmodel.css). 

```css
p {
/* Content- width and height */

/* Border */

border: 2px solid blue;

/* Padding */

/* Margin */

}

```
this gives you border all the way till the end of the line. add `width` property to change that.  
or 
```
width: 50%;
```
this refers to half of the width of the **parenting element**. in this case, it's the `body`. the actual width will change based on the browser width in this case! this is useful.  
```
padding: 10px;
```
this applies to all four sides all the same. what if you want only 2 sides? 
```
padding-left: 40px;
```
these attributes are just like `border-top` attributes for `border`: more specific sub-attribute. actually `border` is the syntactic sugar. 
```
margin: 100px
```
again, this also applies to all 4 sides. 
```
margin-top: 500px;
```
another shortcut:
```
margin: 20px 40px 500px 100px;
```
top, right, bottom, left.  
```
margin: 0 auto 0 auto;
```
this will actually make us in the middle: it automatically give equal to left and right. 
```
margin: 0 auto;
```
this is top/bottom and left/right correspondingly. one tip, you *only* can omit `px` when the number is 0. so similarly: 
```
margin: 20px 50px;
```

### lec60
<img src="https://www.dropbox.com/s/o89ld626hc2eios/Screenshot%202018-04-29%2019.29.01.png?raw=1" width="400">

this is actually a table. selectively turn on off the border. 

### lec61
[board.html](board.html) and [board.css](board.css)

tricky part is to do selectively turn on borders. 

在他讲的过程中, 发现他的这个思路是比较聪明的, 最后他只给[:, 1]这一列, 和[1, :]这一行的这些左右和上下的border, 最后就正好完成这个了; 理解了他这个思路之后, 我自己快速给[1, :]的处理: 
```css
tr:nth-of-type(2) td {
    border-top: 1px solid black;
    border-bottom: 1px solid black;
}
```
注意这里, 这个td要加, 不然不知道为什么不行. 也许tr本身是没有border属性的? 这样讲实际上也讲的通. 不过还是有点搞不清到底什么时候可以继承什么时候不可以; 在[他的答案](board_solution.html)里面你可以看到, 他不是这么做到的. 他是专门重新做了一个class. 

不过他这里展示了一个技巧, 就是[1, 1]这个现在有两个class了: 
```html
<td class="vertical horizontal"></td>
```
就行了. 最后居中: 
```css
table {
    margin: auto;
}
```
注意这里上下的不用写, 默认好像是0的意思; 一个奇怪的小地方: 
```css
h1 {
    text-align: center
}
```
`h1`的居中为什么不能用margin? 我试了一下不行. 好像是因为这些东西自动是block-level? 试了一下, 本身的`margin`是可以用的, 但是就是不能用`auto`. [这里](https://stackoverflow.com/questions/1077173/centering-a-heading-h1)好像大概也提到这个问题, `h1`就是不能用`margin auto`来自动居中, 不知道为什么. 

> The first doesn't work because on inline elements, the automatic margin is zero.  
>   
> margin: auto; does work on inline elements, it just doesn't have the same effect as on block-level elements.  
>   
> (To demonstrate this: if you take an inline element, apply a specific margin to it, and then apply an automatic margin to it, its margin will be zero.)  

<img src="https://www.dropbox.com/s/cg5y4rtemnk4i5p/Screenshot%202018-04-29%2019.58.28.png?raw=1" width="400">

他上课的时候也大概讲了一下, 看这个蓝色的, 就是这个element, 是占用了一整行的. 所以他认为应该调整text; 

### lec63
[photoGrid.html](photoGrid.html) and [photoGrid.css](photoGrid.css)

`div` is block-level element, takes up their own line. 
<img src="https://www.dropbox.com/s/8ixj23ccre9pxi2/Screenshot%202018-04-29%2020.06.16.png?raw=1" width="200">

if I don't want this:
```css
div {
    width: 100px;
    float: left;
}
```
<img src="https://www.dropbox.com/s/w7o4aphgiikq7l9/Screenshot%202018-04-29%2020.06.55.png?raw=1" width="300">

这个float具体的原理还是不是很懂; 当然HTML的render, 本身就是一个从上到下从左到右的Stack操作, 但是这个float是怎么影响这个堆叠的操作的? 

[The element floats to the left of its container](https://www.w3schools.com/cssref/pr_class_float.asp). 

所以有一个*container*的概念; 

<img src="https://www.dropbox.com/s/7yqxl1x8m2d0rdm/Screenshot%202018-04-29%2020.12.26.png?raw=1" width="500">

automatically white space added around images, although we never asked for it. quirks of html, browser added that. use `float` to handle it. 
```css
img {
    width: 100px;
    float: left;
}
```
use percentage to specify `width` here. now add even spacing to this:
<img src="https://www.dropbox.com/s/g1ouurb809pjn7t/Screenshot%202018-04-29%2020.14.39.png?raw=1" width="400">

```css
img {
    width: 30%;
    float: left;
    margin: 1.66%;
}
```
1.66应该是好算出来的. 

### Lec65
```css
p {
    font-family: Raleway;
    margin-left: 1.66%;
    font-size: 23px;
    font-weight: 800;
    text-transform: uppercase;
    border-bottom: 2px solid #f1f1f1;
    width: 30%;
    padding-bottom: 20px;
}
```

### lec66, 67, 68, 69 Blog
[blog.html](blog.html) and [blog.css](blog.css)

generally, only `h1` in one page. If you need more headings, use `h2`. 

```css
body {
    border: 20px solid #bdc3c7;
    width: 700px;
    margin: 20px auto;
    padding: 20px;
}
```
但是这里这个`auto`居然是可以的. 好奇怪; 好像可能是因为是block-level的关系. 我现在的理解是这样的, block-level的element, 默认的`width`是一整行. 所以你单纯设置auto margin没有用. 但是他这里先把`width`缩小了之后, 再用auto, 就没有问题了; 
```css
body {
    border: 20px solid #bdc3c7;
    max-width: 700px;
    width: 80%;
    margin: 20px auto;
    padding: 20px;
}
```
`max` is just a ceiling on `width`. shrink your browser in width to see how that works. 

put each post in its own div for easier management possibily need in the future. 

```
    letter-spacing: 0.2rem;
```
again, relative to the element that they are nested inside. but this time, it's not reletive to the parent element, but to the *root* element of the page. this enables different elements of different nested level to refer to the same data. 

为什么是一个小数? 

`post`这一节课没有用到, 但是这种多保留grouping是一个好习惯; `hr`的styling一般最好是Google一下; 

导入Google字体的另外一种方法: 
```
@import url(https://fonts.googleapis.com/css?family=Source+Sans+Pro:400,700);
```
放在css文件的第一行. 
```
  font-family: 'Source Sans Pro', sans-serif;
```
答案里面这样写不知道是为什么; 

### lec70, 71, 73
boostrap is just a single css file and a single js file. 

[homepage](getbootstrap.com). 

[basics.html](basics.html)

online installing is also available [here](http://getbootstrap.com/docs/3.3/getting-started/#download). eg:
```html
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous">
```

bootstrap is just another css file: as usual, you can override it:
```html
<head>
    <title>Bootstrap Basics</title>
    <link rel="stylesheet" type="text/css" href="bootstrap.css">
    <style type="text/css">
        .btn-danger {
            background: orange;
        }
    </style>
</head>
```
adding classes to existing elements is all what it's about. 
```html
<button class="btn btn-danger btn-xs">CLICK ME!</button>
<button class="btn btn-success btn-xs active">CLICK ME!</button>
<button class="btn btn-success btn-xs" disabled="disabled">CLICK ME!</button>

<a href="http://www.getbootstrap.com" class="btn btn-info btn-lg">Bootstrap Docs</a>
```

### lec74
`jumbotron` is another class that can put to e.g. a `div`. 

<img src="https://www.dropbox.com/s/fpcnp9pltw0pxmd/Screenshot%202018-04-30%2000.08.06.png?raw=1" width="400">

this is no good. this is because jumbotron is setup to take 100% of the size of its container. in this case, the container is nothing, so, fill page. in the grid system, this will become useful.  

for now, do this:
```html
<div class="container">
    <div class="jumbotron">
        <h1>This is a jumbotron</h1>
        <p>Bacon ipsum dolor amet ball tip kevin kielbasa corned beef andouille boudin buffalo pork tenderloin ham hock jerky pancetta beef ribs hamburger. Kielbasa sirloin picanha sausage fatback, prosciutto short ribs chicken venison pork loin frankfurter porchetta tongue cow pig. Swine tri-tip jerky salami ham hock chicken sausage venison flank porchetta rump meatloaf ground round. Shankle tongue meatball capicola strip steak pancetta brisket pig picanha kevin hamburger flank short loin jowl.</p>
        <button class="btn btn-lg btn-success">Hi there</button>
    </div>
</div>
```
this container takes up all space:
<img src="https://www.dropbox.com/s/glz69deu564s64a/Screenshot%202018-04-30%2000.10.13.png?raw=1" width="500">
with large margin. 

sample form for now:
```html
<form>
  <div class="form-group">
    <label for="exampleInputEmail1">Email address</label>
    <input type="email" class="form-control" id="exampleInputEmail1" placeholder="Email">
  </div>
  <div class="form-group">
    <label for="exampleInputPassword1">Password</label>
    <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Password">
  </div>
  <div class="form-group">
    <label for="exampleInputFile">File input</label>
    <input type="file" id="exampleInputFile">
    <p class="help-block">Example block-level help text here.</p>
  </div>
  <div class="checkbox">
    <label>
      <input type="checkbox"> Check me out
    </label>
  </div>
  <button type="submit" class="btn btn-default">Submit</button>
</form>
```
without grid system yet, everything takes the entire line's length. 

```html
  <div class="form-group">
    <label for="exampleInputEmail1">Email address</label>
    <input type="email" class="form-control" id="exampleInputEmail1" placeholder="Email">
  </div>
```
this put the label and inptu together for better spacing.  
when you delete the `form-control` class:
<img src="https://www.dropbox.com/s/wya64mawphrten6/Screenshot%202018-04-30%2000.17.07.png?raw=1" width="400">
so that's why there is a newline between the label and the input. of course you actually lose more effects. there are more important consequences regarding the grid system and the inter-element interaction.  
everything boils down to the two classes: `.form-group` and `.form-control`.  
```html
        <p class="help-block">Example block-level help text here.</p>
```
<img src="https://www.dropbox.com/s/m2b4aug0hunm9vr/Screenshot%202018-04-30%2000.19.10.png?raw=1" width="300">

```html
<form class="form-inline">
  <div class="form-group">
    <label for="exampleInputName2">Name</label>
    <input type="text" class="form-control" id="exampleInputName2" placeholder="Jane Doe">
  </div>
  <div class="form-group">
    <label for="exampleInputEmail2">Email</label>
    <input type="email" class="form-control" id="exampleInputEmail2" placeholder="jane.doe@example.com">
  </div>
  <button type="submit" class="btn btn-default">Send invitation</button>
</form>
```
notice the class `.form-inline`. without this it all goes back to normal html form. 

### lec75 nav bar [navbars.html](navbars.html)
it's very responsive. 

empty link:
```html
<a href="#" class="navbar-brand">Koffee</a>
```

```html
    <div class="nav navbar-nav">
        <li><a href="#">About</a></li>
        <li><a href="#">Contact</a></li>
    </div>
```
this works, but using `ul` is more preferable;  
put everything in the `nav` inside a `container` to avoid no margin against the page edge:
```html
<nav class="navbar navbar-default">
    <div class="container">
        <div class="navbar-header">
            <a href="#" class="navbar-brand">Koffee</a>
        </div>
        <ul class="nav navbar-nav">
            <li><a href="#">About</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
        <ul class="nav navbar-nav navbar-right">
            <li><a href="#">Sign Up</a></li>
            <li><a href="#">Login</a></li>
        </ul>
    </div>
</nav>
```
if you put the `container` outside the `nav`, then the entire navbar will have margins away from the page edge: this is ugly. The right way is to use the `container` to restrict the *content* of the navbar rather than *the navbar itself*.  
the default navbar has the hamburger button when collapsed:
<img src="https://www.dropbox.com/s/j2ope2zug3vvmr4/Screenshot%202018-04-30%2000.38.56.png?raw=1" width="400">
not working for now but we want that. 

the bootstrap js script is put in in the end of the body. but we have error now:
<img src="https://www.dropbox.com/s/6obgngpf1ryzmsw/Screenshot%202018-04-30%2000.41.52.png?raw=1" width="400">
ignore that it is there for now. go to [code.jquery.com](code.jquery.com) to get the latest version. you can get this by searching *jquery CDN*. make sure the jquery's `script` is before `bootstrap.js`'s `script`. now the error is gone. and you see dropdown menus works now. the hamburger works too. 

all those enclosed by `class="collapse navbar-collapse" id="bs-example-navbar-collapse-1"` will collapse when page shrink. 
```html
        <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
            <ul class="nav navbar-nav">
                <li><a href="#">About</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
            <ul class="nav navbar-nav navbar-right">
                <li><a href="#">Sign Up</a></li>
                <li><a href="#">Login</a></li>
            </ul>
        </div>
```
<img src="https://www.dropbox.com/s/klndt1wo0w42bzc/Screenshot%202018-04-30%2000.49.13.png?raw=1" width="300">
goes away. still misses the hamburger.  
this does it:
```html
      <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
        <span class="sr-only">Toggle navigation</span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
      </button>
```
put it in `.navbar-header` but before `.navbar-brand` element. the `target` atttribute will have to match the `id` attribute of the `collapse navbar-collapse` element. 
```html
<nav class="navbar navbar-default">
    <div class="container">
        <div class="navbar-header">
              <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-nav-demo" aria-expanded="false">
                <span class="sr-only">Toggle navigation</span>
                <span class="icon-bar"></span>
                <span class="icon-bar"></span>
                <span class="icon-bar"></span>
              </button>
            <a href="#" class="navbar-brand">Koffee</a>
        </div>
        <div class="collapse navbar-collapse" id="bs-nav-demo">
            <ul class="nav navbar-nav">
                <li><a href="#">About</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
            <ul class="nav navbar-nav navbar-right">
                <li><a href="#">Sign Up</a></li>
                <li><a href="#">Login</a></li>
            </ul>
        </div>
    </div>
</nav>
```
注意看, `target`里面有一个`#`, 但是`id`那里就没有. 有点类似css的select;  
```html
<nav class="navbar navbar-default">
    <div class="container">
        <div class="navbar-header">
              <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-nav-demo" aria-expanded="false">
                <span class="sr-only">Toggle navigation</span>
                <span class="icon-bar"></span>
                <span class="icon-bar"></span>
                <span class="icon-bar"></span>
              </button>
            <a href="#" class="navbar-brand">Koffee</a>
        </div>
        <ul class="nav navbar-nav">
            <li><a href="#">About</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
        <div class="collapse navbar-collapse" id="bs-nav-demo">
            <ul class="nav navbar-nav navbar-right">
                <li><a href="#">Sign Up</a></li>
                <li><a href="#">Login</a></li>
            </ul>
        </div>
    </div>
</nav>
```
Moved About and Contact out, so they stay when page shrunk. this is how you make a navbar anytime: copy that sample code, and figure out what piece you need. 

### lec76 grid system [grid.html](grid.html)

12 is an important number. total 12 colums, then use the grid system to figure out how many each element take out.  
anytime you use a grid, it needs to be in a `container`, start with that. 
```html
<div class="container">
  <div class="row">
    <div class="col-md-6 pink">COL LG 6</div>
    <div class="col-md-6 pink">COL LG 6</div>
  </div>
</div>
```
这个就是做一个一行两列. 上课给的class实际上是`.col-lg-6`. 然后我试了一下, 不行, 自动换行了. 翻了一下Q&A, 好像是因为屏幕的resolution导致的: 我当时是把chrome放在竖屏上面做的, 所以就不行了. 这个有点坑爹. 然后TA给的答案就是`lg`换成`md`或者`sm`. 不知道这个是什么原理; 

at most do 12 `.col-md-1` elements. 

### lec77 grid pt2
4 sizes:
* `lg`: larger
* `md`: laptop
* `sm`: tablet layout
* `xs`: mobile layout

解决竖屏上面用不起来的办法就是可以缩放chrome, 这样就可以正常用了, 80%刚好; 
```html
  <div class="row">
    <div class="col-lg-1 col-md-2 pink">COL LG 1</div>
    <div class="col-lg-1 col-md-2 pink">COL LG 1</div>
    <div class="col-lg-1 col-md-2 pink">COL LG 1</div>
    <div class="col-lg-1 col-md-2 pink">COL LG 1</div>
    <div class="col-lg-1 col-md-2 pink">COL LG 1</div>
    <div class="col-lg-1 col-md-2 pink">COL LG 1</div>
    <div class="col-lg-1 col-md-2 pink">COL LG 1</div>
    <div class="col-lg-1 col-md-2 pink">COL LG 1</div>
    <div class="col-lg-1 col-md-2 pink">COL LG 1</div>
    <div class="col-lg-1 col-md-2 pink">COL LG 1</div>
    <div class="col-lg-1 col-md-2 pink">COL LG 1</div>
    <div class="col-lg-1 col-md-2 pink">COL LG 1</div>
  </div>
```
this means when it's large (browser larger enough), then use `lg-1`. if it get smaller, use `md-2`. the contrast:
<img src="https://www.dropbox.com/s/tbo3bcf10i1x8pn/Screenshot%202018-04-30%2001.23.08.png?raw=1" width="400">

think of all 4 sizes corresponding to 4 break points when you shrink the browser. triggers each size's setting in order. 

when you determine, you want to think what you *want* to happen when you shrink the browser. esp. how many columns do you want displayed: one option is I want 4 columns (4 picture on a row) when large, and still 4 when middle, then 2 when small, and 1 when xs. use this, together with the number 12, to figure out the `class` attributes to put in. 
```html
    <div class="col-lg-3 col-md-3 col-sm-6 pink">TOUR DATA!</div>
```
the `col-lg-3` is not necessary: we are asking it to take 3 units when md, so bootstrap knows that it would be at least 3 units when lg. and we have 4 such elements in total, so no other options. 

nesting:
```html
<div class="container">
  <div class="row">
    <div class="col-md-3 col-sm-6 pink">
      <div class="row">
        <div class="col-lg-6 pink">FIRST HALF</div>
        <div class="col-lg-6 pink">OTHER HALF</div>
      </div>
    </div>
    <div class="col-md-3 col-sm-6 pink">TOUR DATA!</div>
    <div class="col-md-3 col-sm-6 pink">TOUR DATA!</div>
    <div class="col-md-3 col-sm-6 pink">TOUR DATA!</div>
  </div>
</div>
```
note that you can't just do a column inside a column: you have to add in a `row` first: then you have another 12 units (albeit on a smaller scale) to work with. 

### lec79 gallery pt1 [gallery.html](gallery.html)
to add navbars, again, we copy, then pick what we want to keep. 

`navbar-inverse` invert the color the navbar. 
```html
    <div class="row">
        <div class="col-lg-4">
            <div class="thumbnail">
                <img src="http://i.imgur.com/qK42fUu.jpg">
            </div>
        </div>
        <div class="col-lg-4">
            <div class="thumbnail">
                <img src="http://i.imgur.com/qK42fUu.jpg">
            </div>
        </div>
        <div class="col-lg-4">
            <div class="thumbnail">
                <img src="http://i.imgur.com/qK42fUu.jpg">
            </div>
        </div>
    </div>
```
note that this code should be in the same `container` with `jumbotron`. and also, you should see how you use a `thumbnail` to wrap an image: that contains its size: even bootstrap won't do that for you automatically. final note, 这里还是要缩放到80%, 不然还是各种问题; 

now that's 3 images. we want more. we don't have to add another `row`: put them in the one `row`, it will work. 
```html
        <div class="col-lg-4 col-md-6 col-sm-6">
            <div class="thumbnail">
                <img src="https://images.unsplash.com/photo-1442406964439-e46ab8eff7c4?dpr=2&fit=crop&fm=jpg&h=825&q=50&w=1450">
            </div>
        </div>
```
note that the `col-md-6` is again unnecessary. 

add icon:
```html
<span class="glyphicon glyphicon-camera" aria-hidden="true">
```
now let's pint he navbar: you scroll down, you still see it; `navbar-fixed-top` does it, add to the navbar element. 
```css
        body {
            padding-top: 70px;
        }
```
this is just standard padding, bootstrap doc has it: the padding above the jumbotron. 

### lec81 gallery pt2 [gallery.html](gallery.html) [gallery.css](gallery.css)

the glyphicon `<span class="glyphicon glyphicon-camera" aria-hidden="true"></span>` is just text, so it share all the text property settings:
```css
.jumbotron {
    color: #2c3e50;
}
```
this applies to the glyphicon too. 
<img src="https://www.dropbox.com/s/tqw8byodywha2fn/Screenshot%202018-04-30%2014.13.49.png?raw=1" width="400">
want all the text to be white. select `a` won't work. inspect:
<img src="https://www.dropbox.com/s/9e9xfxhqq77uhoh/Screenshot%202018-04-30%2014.14.25.png?raw=1" width="600">
as shown, it's overriden by:
<img src="https://www.dropbox.com/s/vtf78vwjl5pj7zb/Screenshot%202018-04-30%2014.14.52.png?raw=1" width="400">
this wins because it's more specific. you will never know this unless you inspect: which you should do constantly. copy that selector and use it. this **inspect and copy selector** trick is important. 
```css
.navbar-inverse .navbar-nav>li>a {
    color: white;
}

.navbar-inverse .navbar-brand {
    color: white;
}
```
note for the latter one, writing only `navbar-brand` is not enough: it's still less specific than the one `navbar` defaults gives: we are trying to override what bootstrap provides. 

font awesome. install by CDN again. make sure before your own css file's `link`. 
```html
<i class="fas fa-camera-retro"></i>
```
very easy. fontawesome is much richer and more popular than glyphicon. 

### lec82, 83 landing page [purffect-index.html](purffect-index.html) [purffect-index.css](purffect-index.css)

background image:
```
    background: url(https://images.unsplash.com/photo-1415369629372-26f2fe60c467);
    background-size: cover;
```
this makes the image small as possible, while covering the entire window. stretched in both directions. 
```html
<nav class="navbar navbar-default">
  <div class="container-fluid">
```
this is not what we want. we want the content of the `navbar` in a `container`. so change that `container-fluid` to `container`. 
```css
h1, h3 {
    color: white;
}
```
selects union of two. or override everything in `body`: this is safe: any other rule will be more specific and override this. again, some things in `btn` and `navbar` will override our rules, so we have to do inspect and copy again. later on that. now fix the image:
<img src="https://www.dropbox.com/s/jqxddavlfq12j43/Screenshot%202018-04-30%2014.58.08.png?raw=1" width="600">
as you can see, inspect `html` or `body`, the entire height of the `html` stops early: not the full page. we want it to span in height the entire container, which is the window. this split is more clear when you shrink it. 
<img src="https://www.dropbox.com/s/5vdjdw98vi4o6gq/Screenshot%202018-04-30%2014.59.37.png?raw=1" width="400">
easy to fix:
```css
html {
    height: 100%;
}
```
```css
hr {
    width: 400px;
    border-top: 1px solid #f8f8f8;
    border-bottom: 1px solid rgba(0,0,0,0.2);
}
```
this will give the `hr` an effect of the shadow. this `rgba` gives a transparent color. very subtle:
<img src="https://www.dropbox.com/s/db6ix1e0d0wwtid/Screenshot%202018-04-30%2015.01.55.png?raw=1" width="400">
now text shadow:
<img src="https://www.dropbox.com/s/q4y03wrsnoduavm/Screenshot%202018-04-30%2015.05.02.png?raw=1" width="400">
experiments: this adds two shadows, notice the comma:
```css
#content {
    text-align: center;
    padding-top: 25%;
    text-shadow: 0px 4px 3px red, 0px 8px 13px orange;
}
```
<img src="https://www.dropbox.com/s/80hfxa4hz5t9507/Screenshot%202018-04-30%2015.07.27.png?raw=1" width="400">
the three numbers are x offset, y offset, and the blur radius. 不知道什么意思; 

> If you want your bootstrap styled website to be responsive on mobile then be sure to add the following meta tag to your <head>  element, above the <title>  tag:  
> ```html
> <meta name="viewport" content="width=device-width, initial-scale=1">  
> ```
> As a side note, if you can't get the <hr> element to appear correctly on mobile devices then see [here](https://www.udemy.com/the-web-developer-bootcamp/learn/v4/questions/3416722) for a fix.  

## HTML/CSS finishes for now
### lec85,























