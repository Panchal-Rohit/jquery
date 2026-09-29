
---

# 📄 06-ajax.md

Abhi is file me AJAX ka detailed code mat likhna. **Isko intentionally short rakho**, kyunki AJAX hum next step me properly seekhenge.

```markdown
# jQuery AJAX

## 1. What is AJAX?

AJAX allows JavaScript/jQuery to communicate with the server
without reloading the complete webpage.

---

# 2. Normal Form

```text
Form
 ↓
Submit
 ↓
Server
 ↓
Page Reload



3. AJAX Form
Form
 ↓
submit event
 ↓
preventDefault()
 ↓
serialize()
 ↓
AJAX request
 ↓
Laravel
 ↓
Response
 ↓
Update HTML
4. Basic AJAX Structure
$.ajax({

    url: '/students',

    type: 'POST',

    data: formData,

    success: function(response) {

        console.log(response);

    },

    error: function(error) {

        console.log(error);

    }

});

Detailed AJAX learning will be covered separately.


6. Important AJAX Concepts

Next we will learn:

$.ajax()
url
type
data
success
error
beforeSend
complete
JSON response
Laravel routes
Laravel controller
Validation
AJAX CRUD  

