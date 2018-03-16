
### What is JavaScript?
JavaScript is a scripting or programming language that allows you to implement complex things on web pages...

```javascript
var para = document.querySelector('p');

para.addEventListener('click', updateName);

function updateName() {
  var name = prompt('Enter a new name');
  para.textContent = 'Player 1: ' + name;
}
```

* Use javascript to manipulate element

```javascript
  // get/set value of element text
  var value = document.getElementById("demo").innerHTML;
  document.getElementById("demo").innerHTML = "Hello JavaScript";
  
  // set element style
  document.getElementById("demo").style.fontSize = "35px";
```

#### What is a variable?

* A variable is a container for a value, like a number we might use in a sum ...

```javascript
  var name = document.getElementById('name');

  alert('Hello ' + name + ', nice to see you!');
```

* Declaring a variable

```javascript
  var myName;
  var myAge;
```

* Initializing a variable

```javascript
  myName = 'Chris';
  myAge = 37;
```

* Variable types

```javascript
  // Numbers
  var myAge = 17;
  
  // Strings
  var thisIsString = 'I love javascript';
  
  // Booleans
  var iAmAlive = true;
  
  //Arrays
  var myNameArray = ['Chris', 'Bob', 'Jim'];
  var myNumberArray = [10, 15, 40];
  
  console.log(myNameArray[0]); // should return 'Chris'
  console.log(myNumberArray[2]); // should return 40
```

* Objects - `In programming, an object is a structure of code that models a real life object.`

```javascript
  var person = { name : 'Chris', age : 40 };
  
  console.log(person.name) // Chris
  console.log(person.age) // 40
```

![Alt text](https://github.com/ICD0007/javascript-recap/blob/master/operators.png "operators")

#### Comparison operators

* Sometimes we will want to run true/false tests, then act accordingly depending on the result of that test — to do this we use comparison operators.

![Alt text](https://github.com/ICD0007/javascript-recap/blob/master/comparison_operators.png "Comparison operators")

#### Condition statement
```javascript
  var name = prompt('What is your name?');

  if (name === 'James') {
    alert('Hello James, nice to see you!');
  } else if (name === 'John') {
    alert('Hello John, nice to see you!');
  } else if (name === 'Chris') {
    alert('Hello Chris, nice to see you!');
  }
```

#### Looping

```javascript
  var sequence = [1, 1, 2, 3, 5, 8, 13];
  for (var i = 0; i < sequence.length; i++) {
    console.log(sequence[i]);
  }
```

#### JavaScript Events

* HTML events are "things" that happen to HTML elements.

```javascript
  <button onclick="document.getElementById('demo').innerHTML = Date()">The time is?</button>
```
(Comprehensive list here)[https://www.w3schools.com/jsref/dom_obj_event.asp]

#### Project structure
* Create project folder `e.g. javascript-recap`

* Create `index.html` and put the html content below
 
```html
<!DOCTYPE html>
<html>
<head>
    <title>CSS Web Tech Course</title>
    <link rel="stylesheet" type="text/css" href="css/style.css">
</head>
<body>
<div class="container">
    <div class="box-1">
        <h1>Hello World</h1>
        <p>Welcome, put content here...</p>
    </div>

    <div class="box-2">
        <h1>Goodbye World</h1>
        <p>...</p>
        <a class="button" href="">Read More</a>
    </div>

    <div class="categories">
        <h2>Categories</h2>
        <ul>
            <li><a href="#">Category 1</a></li>
        </ul>
        <button>+Add more</button>
    </div>

    <form class="my-form">
        <div class="form-group">
            <label>Name: </label>
            <input type="text" name="name" id="name">
        </div>
        <div class="form-group">
            <label>Email: </label>
            <input type="text" name="email" id="email">
        </div>
        <div class="form-group">
            <label>Message: </label>
            <textarea name="message" id="message"></textarea>
        </div>
        <input class="button" type="submit" value="Submit" name="">
    </form>

</div>

<a class="fix-me button" href="">Hello</a>

<div style="margin-top:500px;"></div>
</body>
</html>
```

#### Link javascript code inside the `head` block

* Inside the folder (`javascript-recap`) created earlier, create another folder `js`,

* Inside this folder `js`, create the javascript file `main.js` that will contain your javascript codes

* Then add the reference to your `index.html` like this - `<script src="js/main.js" type="text/javascript"></script>`

```javascript
  //main.js
  function handleFormSubmit() {
     alert('About to submit');
     console.log('About to submit');
  }
```


### Jquery

* Link jquery to your project `<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>`

#### Basic syntax is: `$(selector).action()`

```javascript
  $(this).hide() - hides the current element.

  $("p").hide() - hides all <p> elements.

  $(".test").hide() - hides all elements with class="test".

  $("#test").hide() - hides the element with id="test".
```

#### The Document Ready Event

```javascript
  $(document).ready(function(){

   // jQuery methods go here...

  });
  
  //or this
  $(function(){

   // jQuery methods go here...

  });
  
  // sample code
  $(document).ready(function(){
    $("button").click(function(){
        $("p").hide();
    });
  });
  
  // get element text
  $("#btn1").click(function(){
    alert("Text: " + $("#test").text());
  });
  
  // get element html
  $("#btn2").click(function(){
      alert("HTML: " + $("#test").html());
  });
```

```html
  <!DOCTYPE html>
  <html>
  <head>
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
  <script>
  $(document).ready(function(){
      $("button").click(function(){
          $("p").hide();
      });
  });
  </script>
  </head>
  <body>

  <h2>This is a heading</h2>

  <p>This is a paragraph.</p>
  <p>This is another paragraph.</p>

  <button>Click me to hide paragraphs</button>

  </body>
  </html>
```

```html
  <!DOCTYPE html>
  <html>
  <head>
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
  <script>
  $(document).ready(function(){
      $("button").click(function(){
          $("#div1").load("demo_test.txt");
      });
  });
  </script>
  </head>
  <body>

  <div id="div1"><h2>Let jQuery AJAX Change This Text</h2></div>

  <button>Get External Content</button>

  </body>
  </html>
```

```javacript
  $("button").click(function(){
      $.get("demo_test.asp", function(data, status){
          alert("Data: " + data + "\nStatus: " + status);
      });
  });
```
