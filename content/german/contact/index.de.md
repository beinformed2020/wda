+++
title = "Kontakt"
layout = "contact"
netlify = false
emailservice = ""
contactanswertime = 24

+++

[**Den Brief finden Sie auf der Titelseite dieser Website.**.](https://worlddoctorsalliance.com/de/)

{{< rawhtml >}}<form id="ajaxForm"
  action="https://getform.io/f/72e0967f-e3ae-46a6-9c11-5da244f57f67"
  method="POST">
  <label>Ihr Name:</label>
  <input type="text" name="name" required/>
    <label>Ihre Rolle? <select name="role[]" >
      <option value="General public">Allgemeine Öffentlichkeit</option>
      <option value="Doctors nurses scientists dentists">Ärzte, Krankenschwestern, Wissenschaftler, Zahnärzte etc.</option>
      <option value="Holistic health practitioners">Ganzheitliche Heilpraktiker</option>
    </select></label>
  <button class="button">Senden</button>

  <p id="my-form-status"></p>

</form>{{< /rawhtml >}}

------

{{< rawhtml >}}

<h2>Mailingliste - Englisch: </h2>

{{< /rawhtml >}}
{{< rawhtml >}}

<form
  action="https://buttondown.email/api/emails/embed-subscribe/wda"
  method="post"
  target="popupwindow"
  onsubmit="window.open('https://buttondown.email/wda', 'popupwindow')"
  class="embeddable-buttondown-form">
  <label for="bd-email">Ihre E-Mail eingeben</label>
  <input type="email" name="email" id="bd-email"></input>
  <input type="hidden" value="1" name="embed"></input>
  <input type="submit" value="Senden"></input>
</form>{{< /rawhtml >}}



------

{{< rawhtml >}}

<h2>Kontaktieren Sie uns:</h2>

{{< /rawhtml >}}

{{< rawhtml >}}<form id="ajaxForm"
  action="https://getform.io/f/a2d75ba7-916c-406f-9b21-9567ecd325b6"
  method="POST">
  <label>Ihr Name:</label>
  <input type="text" name="name" required/>
  <label>Ihre E-Mail:</label>
  <input type="email" name="email" required>
  <label>Ihre Nachricht:</label>
  <input type="textarea" name="message" required>
  <button class="button">Senden</button>

  <p id="my-form-status"></p>

</form>{{< /rawhtml >}}

*Bitte beachten Sie, dass die WMA-Medien von einem kleinen Team von Freiwilligen betrieben werden.  
Wir können nicht auf alle Korrespondenz antworten, aber wir werden sie alle lesen.  
Unsere Standardsprache ist Englisch, andere Sprachen sind für uns schwieriger zu verstehen.  
Wir danken Ihnen.*   

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