
---

# 📄 03-events.md

```markdown
# jQuery Events

## 1. What is an Event?

An event is an action performed by the user or browser.

Examples:

- Click
- Key press
- Form submit
- Select change
- Mouse movement

jQuery allows us to listen for these events.

---

# 2. Click Event

```javascript
$('#btn').click(function() {

    console.log('Button clicked');

});



Flow:

User Click
    ↓
click event
    ↓
function runs
3. Keyup Event
$('#search').keyup(function() {

    let value = $(this).val();

    console.log(value);

});

Useful for:

Search
Live filtering
Live validation
4. Change Event

Used mainly with select/dropdown.

$('#country').change(function() {

    let countryId = $(this).val();

    console.log(countryId);

});

Common use:

Country
 ↓
State
 ↓
City
5. Submit Event
$('#studentForm').submit(function(e) {

    console.log('Form submitted');

});
6. $(this)

this means the current element on which the event occurred.

Example:

$('.deleteBtn').click(function() {

    console.log($(this));

});

If the third delete button is clicked:

this
 ↓
Third delete button
7. Event Object
$('#studentForm').submit(function(e) {

});

e is the event object.

It contains information about the event and provides event methods.

8. preventDefault()

Stops the browser's default action.

Example:

$('#studentForm').submit(function(e) {

    e.preventDefault();

});

Normal:

Submit
 ↓
Browser default action
 ↓
Page may reload

With preventDefault:

Submit
 ↓
preventDefault()
 ↓
Default action stopped
 ↓
JavaScript can handle it





Common Events
Event	Use
click()	Button click
keyup()	Keyboard key release
change()	Input/select value change
submit()	Form submit
mouseenter()	Mouse enters
mouseleave()	Mouse leaves
11. Important Pattern
$('#element').event(function(e) {

    // code

});

Example:

$('#btn').click(function() {

    console.log('Clicked');

});