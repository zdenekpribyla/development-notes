# jQuery Notes

> Personal jQuery codes


### Document ready function
```javascript
//waiting to all document(website) is load
$(document).ready(function() {
  console.log('jQuery is ready!')
})
```

###Basic syntax is: $(selector).action()

+ A <b>$</b> sign to define/access jQuery
+ A <b>(selector)</b> to "query (or find)" HTML elements
+ A jQuery <b>.action()</b> to be performed on the element(s)

####Examples
+ $(this).hide() - hides the current element.
+ $("p").hide() - hides all <p> elements.
+ $(".test").hide() - hides all elements with class="test".
+ $("#test").hide() - hides the element with id="test".

###jQuery event method

####.click()
```javascript
$("p").click(function(){
    // action goes here!!
  });
``` 
####.hide() - (this) remembers the origin selector ("p")
```javascript
$("p").click(function(){
    $(this).hide();
});
```

####.on() - adds one or more event handlers for the selected elements
```javascript
$("p").on({
    mouseenter: function(){
        $(this).css("background-color", "lightgray");
    }, 
    mouseleave: function(){
        $(this).css("background-color", "lightblue");
    }, 
    click: function(){
        $(this).css("background-color", "yellow");
    } 
});
```

####.attr('id') - return the id of the first matched element
```javascript
$('selector').attr('id')
```