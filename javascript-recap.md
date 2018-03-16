
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

#### What is a variable?

* A variable is a container for a value, like a number we might use in a sum ...

```javascript
  var email = document.getElementById('name');

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
```html
<div id="divTest1"></div>
<script type="text/javascript">
$("#divTest1").text("Hello, world!");
</script>
```
