01-selectors.md
# jQuery Selectors

## 1. What is a Selector?

A selector is used to select HTML elements so that we can perform
operations on them using jQuery.

Basic syntax:

```javascript
$('selector')

Example:

$('#name')

This selects the element having id="name".

2. ID Selector

HTML:

<input type="text" id="name">

jQuery:

$('#name')

# is used for ID.

Example:

$('#name').val();
3. Class Selector

HTML:

<div class="box">Hello</div>

jQuery:

$('.box')

. is used for class.

Example:

$('.box').hide();
4. Tag Selector

HTML:

<p>Hello</p>
<p>Welcome</p>

jQuery:

$('p')

This selects all <p> elements.

Example:

$('p').text('Hello Rohit');
5. Multiple Selectors

We can select multiple selectors together.

$('#name, #email')

Example:

$('#name, #email').addClass('active');
6. Attribute Selector

HTML:

<input type="text" name="username">

jQuery:

$('input[name="username"]')

Another example:

$('input[type="email"]')
7. Descendant Selector

HTML:

<div class="user">
    <span class="name">Rohit</span>
</div>

jQuery:

$('.user .name')

This selects .name inside .user.


Common Selectors
Selector	                        Meaning
$('#id')	                        Select by ID
$('.class')	                        Select by class
$('p')	                            Select by tag
$('input')	                        Select all inputs
$('input[name="email"]')	        Select input by attribute
$('.user .name')	                Select name inside user


Remember
#       → ID
.       → Class
tag     → HTML tag
[]      → Attribute

Main idea:

HTML
 ↓
Selector
 ↓
jQuery element
 ↓
Manipulation / Event / Action