# jQuery to Vanilla JavaScript

## Events

```javascript
$(document).ready(function() {

})

document.addEventListener('DOMContentLoaded', function() {

})
```

```javascript
$('a').click(function() {
  
})

[].forEach.call(document.querySelectorAll('a'), function(el) {
  el.addEventListener('click', function() {
    
  })
})
```

## Selectors

```javascript
var divs = $('div')

var divs = document.querySelectorAll('div')
```

```javascript
var newDiv = $('<div/>')

var newDiv = document.createElement('div')
```

## Attributes

```javascript
$('img').filter(':first').attr('alt', 'My image')

document.querySelector('img').setAttribute('alt', 'My image')
```

## Classes

```javascript
newDiv.addClass('foo')

newDiv.classList.add('foo')
```

```javascript
newDiv.toggleClass('foo')

newDiv.classList.toggle('foo')
```

## Manipulation

```javascript
$('body').append($('<p/>'))

document.body.appendChild(document.createElement('p'))
```

```javascript
var clonedElement = $('#about').clone()

var clonedElement = document.getElementById('about').cloneNode(true)
```

```javascript
$('#wrap').empty()

var wrap = document.getElementById('wrap')
while(wrap.firstChild) wrap.removeChild(wrap.firstChild)
```

## Transversing

```javascript
var parent = $('#about').parent()

var parent = document.getElementById('about').parentNode
```

```javascript
if($('#wrap').is(':empty'))

if(!document.getElementById('wrap').hasChildNodes())
```

```javascript
var nextElement = $('#wrap').next()

var nextElement = document.getElementById('wrap').nextSibling
```

## AJAX

### GET
```javascript
$.get('//example.com', function (data) {

})

var httpRequest = new XMLHttpRequest()
httpRequest.onreadystatechange = function (data) {

}
httpRequest.open('GET', url)
httpRequest.send()
```

### POST
```javascript
$.post('//example.com', { username: username }, function (data) {

})

var httpRequest = new XMLHttpRequest()
httpRequest.onreadystatechange = function (data) {

}
httpRequest.setRequestHeader('Content-Type', 'application/x-www-form-urlencoded')
httpRequest.open('POST', url)
httpRequest.send('username=' + encodeURIComponent(username))
```

### JSONP
```javascript
$.getJSON('//openexchangerates.org/latest.json?callback=?', function (data) {

})

function success(data) {
  
}
var scr = document.createElement('script')
scr.src = '//openexchangerates.org/latest.json?callback=formatCurrency'
document.body.appendChild(scr)
```
