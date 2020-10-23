+++
title = "Contact"
layout = "contact"
netlify = false
emailservice = "formspree.io/example@email.com"
contactanswertime = 24

+++

## We are testing a new form system.  
It won't take long.  
Please come back soon.  



{{< rawhtml >}}<p style="text-align:center"><a href="/contact" class="here-button">SIGN OUR OPEN LETTER: CLICK HERE</a></p>

<form id="my-form"
  action="https://formspree.io/f/xzbkrgey"
  method="POST"
>
  <label>Your name:</label>
  <input type="email" name="email" />
    <label>Your Role? <select name="role[]" >
      <option value="General public">General Public</option>
      <option value="Doctors nurses scientists dentists">Doctors, nurses, scientists, dentists etc</option>
      <option value="Holistic health practitioners">Holistic health practitioners</option>
    </select></label>
  <button id="my-form-button">Submit</button>
  <p id="my-form-status"></p>
</form>{{< /rawhtml >}}



<!-- FORMSPREE: Place this script at the end of the body tag -->

<script>
  window.addEventListener("DOMContentLoaded", function() {

    // get the form elements defined in your form HTML above
    
    var form = document.getElementById("my-form");
    var button = document.getElementById("my-form-button");
    var status = document.getElementById("my-form-status");
    
    // Success and Error functions for after the form is submitted
    
    function success() {
      form.reset();
      button.style = "display: none ";
      status.innerHTML = "Thanks!";
    }
    
    function error() {
      status.innerHTML = "Oops! There was a problem.";
    }
    
    // handle the form submission event
    
    form.addEventListener("submit", function(ev) {
      ev.preventDefault();
      var data = new FormData(form);
      ajax(form.method, form.action, data, success, error);
    });
  });

  // helper function for sending an AJAX request

  function ajax(method, url, data, success, error) {
    var xhr = new XMLHttpRequest();
    xhr.open(method, url);
    xhr.setRequestHeader("Accept", "application/json");
    xhr.onreadystatechange = function() {
      if (xhr.readyState !== XMLHttpRequest.DONE) return;
      if (xhr.status === 200) {
        success(xhr.response, xhr.responseType);
      } else {
        error(xhr.status, xhr.response, xhr.responseType);
      }
    };
    xhr.send(data);
  }
</script>