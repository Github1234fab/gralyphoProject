<script>
  import { onMount } from "svelte";
  import Gralypho from "../Components/Gralypho.svelte";

  let Year;

  onMount(() => {
    Year = new Date().getFullYear();
  });
</script>

<footer class="footer">
  <div class="wrapper-gralypho">
    <div class="gralypho">
      <Gralypho />
    </div>
  </div>
  <!-- <div class="wrapper-contact">
    <a href="mailto:gralypho@gmail.com " class="contact">contact@gralypho.com</a>
    <a href="tel:0672901614" class="contact">0672 901 614</a>
  </div> -->
  <div class="wrapper-contactez">
      <a href="mailto:gralypho@gmail.com " class="contact"><i class="fa-regular fa-envelope"></i></a>
      <a href="tel:0672901614" class="contact"><i class="fa-solid fa-phone-volume"></i></a>
      <a href="tel:0672901614" class="contact"><i class="fa-solid fa-mug-hot"></i></a>
    </div>


  <div class="wrapper-media">
    <a href="https://www.facebook.com/" target="_blank"><i class="fa-brands fa-square-facebook anim"></i></a>
    <a href="https://twitter.com/home?lang=fr" target="_blank"><i class="fa-brands fa-square-twitter anim"></i></a>
    <a href="https://www.instagram.com/" target="_blank"><i class="fa-brands fa-square-instagram anim"></i></a>
    <a href="https://www.tiktok.com/fr/" target="_blank"><i class="fa-brands fa-tiktok anim"></i></a>
  </div>
  <h4>© {Year} GRALYPHO. <br /> Tous droits réservés.</h4>
</footer>

<style>
  .footer {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100%;
    font-size: 16px;
    background-color: var(--primary);
    color: white;
    font-family: epilogue;
    padding: 70px;
    gap: 0px;
  }
  .footer h4 {
    margin-top: 30px;
    font-family: epilogue;
    font-weight: 400;
    font-size: 0.6em;
    color: var(--colorC);
    text-align: center;
  }
  .wrapper-gralypho {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto;
  }
  .gralypho {
    margin-left: 30px;
  }
  .wrapper-contactez{
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    text-align: center;
    /* background-color: var(--CTA); */
    border-radius: 8px;
    padding: 40px;
    gap: 4px;
  }
  .contact {
    text-decoration: none;
    color: white;
    font-size: 1em;
    font-family: poppins;
    width: 100%;
    transform: rotate(0deg);
    transition: 0.2s ease-in-out;
    border-radius: 8px;
    border: 1px solid var(--CTA);
    padding: 15px;
    background-color: var(--CTA);

  }
  .contact:hover {
    animation: bounce 0.4s ease-in-out;
font-weight: 800;
  }

  a {
    color: var(--CTA);
    font-size: 1.8em;
    margin: 0 0px;
    transition: 0.4s ease-in-out;
  }

  .anim:hover {
    animation: bounce 0.4s ease-in-out;
  }
  @keyframes bounce {
    0% {
      transform: scale(1) translateY(-2px);
    }
    25% {
      transform: scale(1) translateY(3px);
    }
    50% {
      transform: scale(1) translateY(-1px);
    }
    75% {
      transform: scale(1) translateY(2px);
    }
    100% {
      transform: scale(1) translateY(0);
    }
  }
  .wrapper-media {
    display: flex;
    gap: 10px;
  }
</style>
