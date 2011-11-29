Description
===========

textSaver is a jQuery plugin that uses HTML5 localStorage (aka "Web Storage") to store what your users enter into input text fields or textareas. That's it! No messy cookies, session IDs, or database calls needed—this means that your users' draft versions of forms will be as secure as their computers, since nothing but the final submission is sent to a server. This saves space on your own servers and reduces the chances for XSS attacks.

Usage
======

The best practice is to call .textSaver() on a form. This way, all input text fields and textareas will be saved, and localStorage will clear when the form is submitted.

The form:
```html
<form id="the_form">
  <input type="text" id="name" name="name" />
  <textarea id="big_textarea" name="big_textarea" rows="23" cols="42"></textarea>
  <input type="submit" value="Submit" />
</form>
```

The jQuery:
```javascript
$(document).ready(function() {
  $("#the_form").textSaver();
});
```

Nevertheless, .textSaver() can still be called on individual textareas or input text fields if you only want certain fields to be savable.