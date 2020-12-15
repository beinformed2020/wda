+++
title = "Contacto"
layout = "contact"
netlify = false
emailservice = ""
contactanswertime = 24

+++

[**Por favor, encuentre la carta en la página principal de este sitio web**.](https://worlddoctorsalliance.com/es/)

{{< rawhtml >}}<form id="ajaxForm"
  action="https://getform.io/f/72e0967f-e3ae-46a6-9c11-5da244f57f67"
  method="POST">
  <label>Su nombre:</label>
  <input type="text" name="name" required/>
    <label>Su papel? <select name="role[]" >
      <option value="General public">Público en general</option>
      <option value="Doctors nurses scientists dentists">Médicos, enfermeras, científicos, dentistas etc</option>
      <option value="Holistic health practitioners">Profesionales de la salud holística</option>
    </select></label>
  <button class="button">Enviar</button>

  <p id="my-form-status"></p>

</form>{{< /rawhtml >}}

------

{{< rawhtml >}}

<h2>Lista de correo - Inglés: </h2>

{{< /rawhtml >}}
{{< rawhtml >}}

<form
  action="https://buttondown.email/api/emails/embed-subscribe/wda"
  method="post"
  target="popupwindow"
  onsubmit="window.open('https://buttondown.email/wda', 'popupwindow')"
  class="embeddable-buttondown-form">
  <label for="bd-email">Su correo electrónico</label>
  <input type="email" name="email" id="bd-email"></input>
  <input type="hidden" value="1" name="embed"></input>
  <input type="submit" value="Suscríbete"></input>
</form>{{< /rawhtml >}}




------

{{< rawhtml >}}

<h2>Contactarnos:</h2>

{{< /rawhtml >}}

{{< rawhtml >}}<form id="ajaxForm"
  action="https://getform.io/f/a2d75ba7-916c-406f-9b21-9567ecd325b6"
  method="POST">
  <label>Su nombre:</label>
  <input type="text" name="name" required/>
  <label>Su correo electrónico</label>
  <input type="email" name="email" required>
  <label>Su mensaje:</label>
  <input type="textarea" name="message" required>
  <button class="button">Enviar</button>

  <p id="my-form-status"></p>

</form>{{< /rawhtml >}}

------

*Por favor, tenga en cuenta que los medios de comunicación de la AMM están dirigidos por un pequeño equipo de voluntarios.  
No podemos responder a toda la correspondencia, pero la leeremos toda.  
Nuestro idioma por defecto es el Inglés, otros idiomas son más difíciles de entender para nosotros.  
Gracias.*   

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