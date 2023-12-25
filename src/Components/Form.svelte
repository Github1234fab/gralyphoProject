<!-- <script>
  import { onMount } from 'svelte';
  import emailjs from 'emailjs-com';

  let name = '';
  let email = '';
  let message = '';

  const YOUR_SERVICE_ID = 'your_service_id'; // Remplacez par votre ID de service EmailJS

  let captchaToken = '';

  function onSubmit(event) {
    event.preventDefault();
    // Vérifiez le captcha ici
    if (captchaToken) {
      emailjs.send(YOUR_SERVICE_ID, 'template_id', {
        from_name: name,
        message: `${email} says ${message}`,
      })
      .then((response) => {
        console.log('SUCCESS!', response.status, response.text);
      }, (error) => {
        console.log('FAILED...', error);
      });
    } else {
      console.log('Captcha non valide');
    }
  }

  onMount(() => {
    // Initialiser le reCAPTCHA
    grecaptcha.ready(() => {
      grecaptcha.execute('your_site_key', { action: 'submit' }).then((token) => {
        captchaToken = token;
      });
    });
  });
</script>

<form on:submit={onSubmit}>
  <label>
    Name:
    <input type="text" bind:value={name} />
  </label>
  <label>
    Email:
    <input type="email" bind:value={email} />
  </label>
  <label>
    Message:
    <textarea bind:value={message}></textarea>
  </label>
  <div class="g-recaptcha" data-sitekey="your_site_key" data-callback="onSubmit" data-action="submit"></div>
  <button type="submit">Submit</button>
</form> -->

<!-- <script src="https://www.google.com/recaptcha/api.js" async defer></script>
<script src="https://cdn.emailjs.com/dist/email.min.js" type="text/javascript"></script> -->
