# JQUERY MINI PROJECT - SIMPLE NOTES

1. $(document).ready()

---

$(document).ready(function () {

});

→ Page load hone ke baad jQuery code run karta hai.

2. let students = []

---

let students = [];

→ Students ka temporary data store karta hai.

3. let editIndex = null

---

let editIndex = null;

→ Kaunsa student edit ho raha hai uska index store karta hai.

null = Add mode
number = Edit mode

4. submit()

---

$('#studentForm').submit(function(e) {

});

→ Form submit hone par function run karta hai.

5. preventDefault()

---

e.preventDefault();

→ Form ka default submit aur page reload rokta hai.

6. val()

---

let name = $('#name').val();

→ Input ki value get karta hai.

$('#name').val('Rohit');

→ Input ki value set karta hai.

7. trim()

---

let name = $('#name').val().trim();

→ Extra spaces remove karta hai.

8. text()

---

$('#error').text('Name is required');

→ Element me text set karta hai.

let text = $('#error').text();

→ Element ka text get karta hai.

9. html()

---

$('#box').html('<b>Hello</b>');

→ Element ke andar HTML set karta hai.

10. attr()

---

$('#photo').attr('src', 'new.jpg');

→ HTML attribute change karta hai.

11. addClass()

---

$('#box').addClass('active');

→ Class add karta hai.

12. removeClass()

---

$('#box').removeClass('active');

→ Class remove karta hai.

13. toggleClass()

---

$('#box').toggleClass('active');

→ Class ko add/remove karta hai.

14. show()

---

$('#box').show();

→ Element show karta hai.

15. hide()

---

$('#box').hide();

→ Element hide karta hai.

16. toggle()

---

$('#box').toggle();

→ Show/Hide karta hai.

17. append()

---

$('#list').append('<li>Rohit</li>');

→ Element ke end me HTML add karta hai.

18. prepend()

---

$('#list').prepend('<li>Rohit</li>');

→ Element ke start me HTML add karta hai.

19. remove()

---

$('.user').remove();

→ Selected element ko remove karta hai.

20. empty()

---

$('#list').empty();

→ Element ke andar ka content remove karta hai.

Difference:

remove()
→ Element bhi delete

empty()
→ Element rahega, andar ka content delete

21. parent()

---

$('.name').parent();

→ Parent element find karta hai.

22. children()

---

$('.user').children();

→ Direct child elements find karta hai.

23. find()

---

$('.user').find('.name');

→ Element ke andar matching element find karta hai.

24. $.each()

---

$.each(students, function(index, student) {

});

→ Array ke items ko one by one process karta hai.

index = position
student = current item

25. click()

---

$('#btn').click(function() {

});

→ Button click hone par function run karta hai.

26. keyup()

---

$('#search').keyup(function() {

});

→ Keyboard key release hone par function run karta hai.

27. change()

---

$('#country').change(function() {

});

→ Input/select ki value change hone par function run karta hai.

28. $(this)

---

$(this)

→ Current element ko represent karta hai.

Example:

$('.deleteBtn').click(function() {

    $(this);

});

→ Jis delete button par click hua.

29. data()

---

let index = $(this).data('index');

→ data-index ki value get karta hai.

HTML:

<button data-index="2">Delete</button>

Result:

index = 2

30. serialize()

---

let formData = $('#studentForm').serialize();

→ Pure form ka data ek saath collect karta hai.

Example:

name=Rohit&email=rohit@gmail.com

.val()
→ Ek field ki value

.serialize()
→ Pure form ka data

31. push()

---

students.push(student);

→ Array me new student add karta hai.

32. splice()

---

students.splice(index, 1);

→ Array se student delete karta hai.

splice(startIndex, deleteCount)

33. indexOf()

---

let index = students.indexOf(student);

→ Student ka array index find karta hai.

34. filter()

---

let result = students.filter(function(student) {

    return student.name.includes('Rohit');

});

→ Matching students ki new array banata hai.

35. includes()

---

student.name.includes('Rohit');

→ Check karta hai ki text ke andar value exist karti hai ya nahi.

true / false

36. focus()

---

$('#name').focus();

→ Input par cursor/focus le jata hai.

37. reset()

---

$('#studentForm')[0].reset();

→ Complete form clear karta hai.

38. confirm()

---

if (confirm('Are you sure?')) {

}

→ Confirmation popup show karta hai.

OK → true
Cancel → false

39. renderStudents()

---

function renderStudents(list = students) {

}

→ Students ko HTML table me display karta hai.

Basic flow:

students
↓
$.each()
↓
append()
↓
HTML Table

40. renderStudents()

---

$('#studentList').empty();

→ Purani table rows remove.

$.each(list, function(index, student) {

    $('#studentList').append(`
        <tr>
            <td>${student.name}</td>
        </tr>
    `);

});

→ Har student ki table row create.

41. DELETE FLOW

---

Delete button
↓
data-index
↓
.data('index')
↓
confirm()
↓
splice()
↓
renderStudents()

42. EDIT FLOW

---

Edit button
↓
data-index
↓
students[index]
↓
.val()
↓
Form fill
↓
editIndex
↓
Update student
↓
renderStudents()

43. SEARCH FLOW

---

Search input
↓
keyup()
↓
.val()
↓
filter()
↓
includes()
↓
renderStudents()

44. FORM FLOW

---

Submit
↓
submit()
↓
preventDefault()
↓
Get values
↓
Validation
↓
serialize()
↓
Add / Update
↓
renderStudents()

45. IMPORTANT DIFFERENCE

---

.val()
→ Input ki value

.text()
→ Text

.html()
→ HTML

.attr()
→ Attribute

.append()
→ End me add

.prepend()
→ Start me add

.remove()
→ Element delete

.empty()
→ Element ke andar ka content delete

$.each()
→ One by one loop

.filter()
→ Matching data filter

.push()
→ Array me add

.splice()
→ Array se delete

.serialize()
→ Complete form data

.preventDefault()
→ Default form submit stop

## FINAL FLOW

jQuery
↓
Selectors
↓
DOM Manipulation
↓
Events
↓
Form
↓
preventDefault()
↓
serialize()
↓
AJAX
↓
Laravel
