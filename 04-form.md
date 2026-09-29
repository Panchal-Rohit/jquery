
---

# 📄 04-form.md

```markdown
# jQuery Forms

## 1. Form Handling

jQuery can be used to:

- Read form values
- Validate form
- Prevent normal submit
- Collect form data
- Submit data using AJAX

---

# 2. Basic Form

```html
<form id="studentForm">

    <input
        type="text"
        id="name"
        name="name"
    >

    <input
        type="email"
        id="email"
        name="email"
    >

    <button type="submit">
        Save
    </button>

</form>



Get Input Value
let name = $('#name').val();
4. Form Submit
$('#studentForm').submit(function(e) {

});
5. Prevent Default
$('#studentForm').submit(function(e) {

    e.preventDefault();

});

Meaning:

Stop the browser's normal form submission.

6. Form Validation
$('#studentForm').submit(function(e) {

    e.preventDefault();

    let name = $('#name').val();

    if (name === '') {

        $('#error').text('Name is required');

        return;
    }

});

Flow:

Submit
 ↓
preventDefault()
 ↓
Get value
 ↓
Validate
 ↓
If invalid → show error
 ↓
If valid → continue
7. Reset Form

Native JavaScript reset:

$('#studentForm')[0].reset();

This clears the form fields.

8. Clear Error
$('#error').text('');



10. Important Difference
.val()
 ↓
One input value

.serialize()
 ↓
Complete form data
11. Important Rule

For form submission, input fields should have name.

Correct:

<input
    id="email"
    name="email"
>

The id is useful for selecting the element.

The name is important for form data.