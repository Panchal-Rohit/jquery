---

# 📄 02-dom-manipulation.md

```markdown
# jQuery DOM Manipulation

## 1. What is DOM Manipulation?

DOM manipulation means changing HTML elements using JavaScript/jQuery.

Examples:

- Change text
- Change HTML
- Change input value
- Change attributes
- Add/remove classes
- Add/remove elements
- Show/hide elements

---

# 2. `.val()`

Used to get or set the value of form elements.

## Get Value

HTML:

```html
<input type="text" id="name" />

jQuery: let name = $('#name').val(); Set Value $('#name').val('Rohit');
Remember: .val() ↓ Input / Select value 3. .text() Used to get or set text.
HTML:

<p id="message">Hello</p>

Set: $('#message').text('Hello Rohit'); Get: let message = $('#message').text();
4. .html() Used to get or set HTML. $('#message').html('<b>Hello Rohit</b>');
Difference: .text() ↓ Plain text .html() ↓ HTML content 5. .attr() Used to get
or change HTML attributes. HTML:

<img id="photo" src="old.jpg" />

Get: let src = $('#photo').attr('src'); Set: $('#photo').attr('src', 'new.jpg');
6. .addClass() $('#box').addClass('active'); Adds a class. 7. .removeClass()
$('#box').removeClass('active'); Removes a class. 8. .toggleClass()
$('#box').toggleClass('active'); If class exists → removes it. If class does not
exist → adds it. 9. .show() $('#box').show(); Shows the element. 10. .hide()
$('#box').hide(); Hides the element. 11. .toggle() $('#box').toggle(); Toggles
between show and hide. 12. .append() Adds HTML at the end. HTML:

<ul id="users"></ul>

jQuery: $('#users').append('
<li>Rohit</li>
'); Result:

<ul id="users">
  <li>Rohit</li>
</ul>
13. .prepend() Adds HTML at the beginning. $('#users').prepend('
<li>Rohit</li>
'); 14. .remove() Completely removes the selected element. $('.user').remove();
15. .empty() Removes only the inside content. $('#userList').empty();
Difference: .remove() ↓ Element itself removed .empty() ↓ Element remains Inside
content removed 16. .parent() Gets the direct parent. $('.name').parent(); 17.
.children() Gets direct children. $('.user').children(); 18. .find() Searches
elements inside another element. $('.user').find('.name'); Difference:
children() ↓ Direct child find() ↓ Any matching descendant
```


Quick Revision
.val()                          → input value
.text()                         → text
.html()                         → HTML
.attr()                         → attribute

addClass()                      → add class
removeClass()                   → remove class
toggleClass()                   → toggle class

show()                          → show
hide()                          → hide
toggle()                        → show/hide

append()                        → add at end
prepend()                       → add at beginning

remove()                        → remove element
empty()                         → remove inside content

parent()                        → parent
children()                      → direct children
find()                          → search inside