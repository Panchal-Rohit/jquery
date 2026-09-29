
---

# 📄 05-serialize.md

```markdown
# jQuery Serialize

## 1. What is `.serialize()`?

`.serialize()` collects form fields into a request-friendly string.

Example:

```javascript
let formData = $('#studentForm').serialize();


Example Form
<form id="studentForm">

    <input
        type="text"
        name="name"
        value="Rohit"
    >

    <input
        type="email"
        name="email"
        value="rohit@gmail.com"
    >

    <input
        type="text"
        name="city"
        value="Saharanpur"
    >

</form>

jQuery:

let formData = $('#studentForm').serialize();

console.log(formData);

Output:

name=Rohit&email=rohit%40gmail.com&city=Saharanpur
3. Why Use Serialize?

Without serialize:

let name = $('#name').val();
let email = $('#email').val();
let phone = $('#phone').val();
let city = $('#city').val();

For 10 fields, this becomes repetitive.

With serialize:

let formData = $('#studentForm').serialize();

All form data is collected together.

4. .val() vs .serialize()
.val()
 ↓
One field

.serialize()
 ↓
Complete form

Example:

let name = $('#name').val();

Only name.

But:

let formData = $('#studentForm').serialize();

Complete form.

5. Why name Attribute Matters?

Correct:

<input
    id="name"
    name="name"
>

Incorrect for serialization:

<input
    id="name"
>

serialize() works with successful form controls that have a name.

6. Serialize + Submit
$('#studentForm').submit(function(e) {

    e.preventDefault();

    let formData = $(this).serialize();

    console.log(formData);

});
7. Why Use $(this)?

Inside the submit event:

$(this)

means:

The form that triggered the submit event.

So:

$(this).serialize();

means:

Serialize this submitted form.


9. Important Point

.serialize() does NOT save data to the database.

It only collects/formats the form data.

serialize()
 ↓
Collect data
 ↓
AJAX
 ↓
Laravel
 ↓
Database
10. Remember
let formData = $(this).serialize();

This is a very common pattern in jQuery AJAX forms.