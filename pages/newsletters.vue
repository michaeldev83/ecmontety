<template>
  <div class="main">
    <section class="newsletters">
      <!-- Begin Mailchimp Signup Form -->
      <link href="//cdn-images.mailchimp.com/embedcode/classic-10_7.css" rel="stylesheet" type="text/css">

      <div id="mc_embed_signup">
        <form
          id="mc-embedded-subscribe-form"
          :action="lien"
          name="mc-embedded-subscribe-form"
          method="post"
          class="validate"
          novalidate
        >
          <div id="mc_embed_signup_scroll">
            <h2>Inscription à la newsletter</h2>
            <div id="mce-responses" class="clear">
              <div
                id="mce-error-response"
                class="response"
              >
              </div>
              <div
                id="mce-success-response"
                class="response"
              >
              </div>
            </div>
            <div class="indicates-required">
              <span class="asterisk">*</span> indicates required
            </div>
            <div class="mc-field-group">
              <label for="mce-EMAIL">
                Adresse Email  <span class="asterisk">*</span>
              </label>
              <input id="mce-EMAIL" type="email" value="" name="EMAIL" class="required email">
            </div>
            <div class="mc-field-group">
              <label for="mce-FNAME">
                Nom du joueur (enfant)  <span class="asterisk">*</span>
              </label>
              <input id="mce-FNAME" type="text" value="" name="FNAME" class="required">
            </div>
            <!-- real people should not fill this in and expect good things - do not remove this or risk form bot signups-->
            <div style="position: absolute; left: -5000px;" aria-hidden="true"><input type="text" name="b_b966386b08d71cc311ca4af74_fabedda210" tabindex="-1" value=""></div>
            <div class="clear"><input id="xmc-embedded-subscribe" type="submit" value="S'abonner" name="subscribe" class="btn"></div>
          </div>
        </form>
      </div>
      <script type="text/javascript" src="//s3.amazonaws.com/downloads.mailchimp.com/js/mc-validate.js">
      </script>
      <script type="text/javascript">
        (function($) {
        window.fnames = new Array();
        window.ftypes = new Array();
        fnames[0]='EMAIL';
        ftypes[0]='email';
        fnames[1]='FNAME';
        ftypes[1]='text';
        /*
        * Translated default messages for the $ validation plugin.
        * Locale: FR
        */
        $.extend($.validator.messages, {
        required: "Ce champ est requis.",
        remote: "Veuillez remplir ce champ pour continuer.",
        email: "Veuillez entrer une adresse email valide.",
        url: "Veuillez entrer une URL valide.",
        date: "Veuillez entrer une date valide.",
        dateISO: "Veuillez entrer une date valide (ISO).",
        number: "Veuillez entrer un nombre valide.",
        digits: "Veuillez entrer (seulement) une valeur numérique.",
        creditcard: "Veuillez entrer un numéro de carte de crédit valide.",
        equalTo: "Veuillez entrer une nouvelle fois la même valeur.",
        accept: "Veuillez entrer une valeur avec une extension valide.",
        maxlength: $.validator.format("Veuillez ne pas entrer plus de {0} caractères."),
        minlength: $.validator.format("Veuillez entrer au moins {0} caractères."),
        rangelength: $.validator.format("Veuillez entrer entre {0} et {1} caractères."),
        range: $.validator.format("Veuillez entrer une valeur entre {0} et {1}."),
        max: $.validator.format("Veuillez entrer une valeur inférieure ou égale à {0}."),
        min: $.validator.format("Veuillez entrer une valeur supérieure ou égale à {0}.")
        });
        }(jQuery));
        var $mcj = jQuery.noConflict(true);
      </script>
      <!--End mc_embed_signup-->
    </section>

    <p class="note">
      <span><b>Note Importante:</b></span> <br><br>
      La newsletter ne servira qu'à envoyer des emails concernants les actualités du site et les convocations, <b>en aucun cas vous ne recevrez des emails à des fins commerciales</b>. <br><br>
      Pensez à regarder vos <b>courriers indésirables</b> pour certaines boites emails.
    </p>
  </div>
</template>

<script>
export default {
  data () {
    return {
      lien: 'https://app.us5.list-manage.com/subscribe/post?u=b966386b08d71cc311ca4af74&id=fabedda210'
    }
  }
}
</script>

<style scoped>
.newsletters {
  position:relative;
  top:150px;
  width:100%;
  padding:10px 10px 30px;
  box-shadow: 0px 0px 2px 2px rgba(0,0,0,0.2);
  border-radius: 10px;
  margin-bottom: 10px;
}
.note {
  position:relative;
  top: 140px;
  margin: 30px 0;
  padding: 15px;
}
b:nth-child(1) {
  text-decoration: underline;
}
#mc_embed_signup {
  background:#fff;
  clear:left;
  font:16px Helvetica,Arial,sans-serif;
}
.btn {
  border: none!important;
  transition: all 0.23s ease-in-out 0s;
  color: #FFFFFF;
  cursor: pointer;
  font-size: 15px;
  font-weight: normal;
  height: 32px;
  line-height: 32px;
  padding: 0 22px;
  text-align: center;
  text-decoration: none;
  vertical-align: top;
  white-space: nowrap;
  background-color: #3b5997;
}
.btn:hover {
  background-color:#4c72bd;
}
.response{
  display:none;
}
</style>
