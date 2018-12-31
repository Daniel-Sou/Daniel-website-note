# JAVASCRIPT AND THE DOM
## Review
In this lesson, you manipulated a webpage structure by leveraging the Document Object Model interface in JavaScript.

Let's review what we learned:

- The document keyword grants access to the root of the DOM in JavaScript
- The DOM Interface allows you to select a specific element with CSS selectors by using the `.querySelector()` method
- You can also access an element directly by its ID with `.getElementById()`
- The `.innerHTML` and `.style` properties allow you to modify an element by changing its contents or style respectively
- You can create, append, and remove elements by using the `.createElement()`,`.appendChild()` and `.removeChild()` methods respectively
- The `.onclick` property can add interactivity to a DOM element based on a click event

Picture:
![845e48821d9decdf48f84d4025c0097c.png](evernotecid://423064E1-7D9D-4304-BB9F-F1EB29FF109D/appyinxiangcom/21310654/ENResource/p810)


## Tweak an element

Change the HTML element
```
document.body.innerHTML = 'The cat loves the dog.';
```

## Select and Modify Element
.querySelector()

CSS selector:
- .class
- #ID
```
document.querySelector('p');
```
Directly by id
```
document.getElementById('bio').innerHTML = 'The description';
```

## Style an element
.style - CSS style
```
let blueElement = document.querySelector('.blue');
blueElement.style.backgroundColor = 'blue';

or

document.querySelector('.blue').style.fontFamily = 'Roboto';
```

## Create and Insert Elements
`.createElement(tagName)` create the new element
`.appendChild()` add a child element
`innerHTML` add text to new element

Example
```
let paragraph = document.createElement('p');
paragraph.innerHTML = 'The text inside paragraph';
document.body.appendChild(paragraph);

or

let list = document.createElement('li');
list.id = "oaxaca";
list.innerHTML = "Oaxaca Mexico";

document.getElementById('more-destinations').appendChild(list);
```

## Remove an Element
`.removeChild()` removes a specified child from a parent

Example
```
let paragraph = document.querySelector('p');
document.body.removeChild(paragraph);

or 

let child = document.querySelector('#oaxaca');

let parent = document.querySelector('#more-destinations');

parent.removeChild(child);
```
Hide an element
```
document.getElementById('sign').hidden = true;
```
## Interactivity with onclick
Example
```
let element = document.getElementById('interact');
element.onclick = function() { element.style.backgroundColor = 'blue' };
```

Example Exercise
```
let element = document.querySelector("button");

function turnButtonRed (){
	element.style.backgroundColor = "red";
  element.style.color = "white";
  element.innerHTML = "Red Button"; 
}

element.onclick = turnButtonRed;
```

## Traversing the DOM
`.parentNode` is node towards the root
`.childNode` is node away from the root

Example Exercise
```
let first = document.body.firstChild;

first.innerHTML = 'I am the child!'

first.parentNode.innerHTML = 'I am the parent and my inner HTML has been replaced!'
```


