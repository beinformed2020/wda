+++
title = "Contact"
layout = "contact"
netlify = false
emailservice = "formspree.io/example@email.com"
contactanswertime = 24

+++
{{< rawhtml >}}<form id="ajaxForm"
  action="https://getform.io/f/72e0967f-e3ae-46a6-9c11-5da244f57f67"
  method="POST"

>
  <label>Your name:</label>
  <input type="text" name="name" required/>
    <label>Your Role? <select name="role[]" >
      <option value="General public">General Public</option>
      <option value="Doctors nurses scientists dentists">Doctors, nurses, scientists, dentists etc</option>
      <option value="Holistic health practitioners">Holistic health practitioners</option>
    </select></label>
  <button class="button">Submit</button>
  <p id="my-form-status"></p>
</form>{{< /rawhtml >}}
{{< rawhtml >}}

<h2>Sign-up for our mailing list</h2>
{{< /rawhtml >}}
{{< rawhtml >}}

<form
  action="https://buttondown.email/api/emails/embed-subscribe/wda"
  method="post"
  target="popupwindow"
  onsubmit="window.open('https://buttondown.email/wda', 'popupwindow')"
  class="embeddable-buttondown-form"
>
  <label for="bd-email">Enter your email</label>
  <input type="email" name="email" id="bd-email"></input>
  <input type="hidden" value="1" name="embed"></input>
  <input type="submit" value="Subscribe"></input>
</form>{{< /rawhtml >}}
<!-- Getform: Place this script at the end of the body tag -->

<script>

```
$("#ajaxForm").submit(function(e){
  e.preventDefault();
  var action = $(this).attr("action");
  $.ajax({
    type: "POST",
    url: action,
    crossDomain: true,
    data: new FormData(this),
    dataType: "json",
    contentType: "multipart/form-data",
    processData: false,
    contentType: false,
    headers: {
      "Accept": "application/json"
    }
  }).done(function() {
     $('.success').addClass('is-active');
  }).fail(function() {
     alert('An error occurred please try again later.')
  });
});
```


</script>