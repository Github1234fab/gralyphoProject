<script>
  import { onMount } from "svelte";
  import Gralypho from "../Components/Gralypho.svelte";

  let Year;

  onMount(() => {
    Year = new Date().getFullYear();
  });
</script>

<footer class="footer">

  <div class="wrapper-contact">
    <Gralypho/>
    <a href="mailto:gralypho@gmail.com " class="contact">gralypho@gmail.com</a>
    <a href="tel:0672901614" class="contact">06 72 90 16 14</a>
  </div>

  <div class="wrapper-media">
    <a
      href="https://www.facebook.com/"
      target="_blank"><i class="fa-brands fa-square-facebook anim"></i></a
    >
    <a
      href="https://twitter.com/home?lang=fr"
      target="_blank"><i class="fa-brands fa-square-twitter anim"></i></a
    >
    <a
      href="https://www.instagram.com/"
      target="_blank"><i class="fa-brands fa-square-instagram anim"></i></a
    >
    <a
      href="https://www.tiktok.com/fr/"
      target="_blank"><i class="fa-brands fa-tiktok anim"></i></a
    >
  </div>
  <h4>© {Year} GRALYPHO. <br /> Tous droits réservés.</h4>
</footer>

<style>
  .footer {
    height: 100%;
    font-size: 16px;
    background-color: var(--colorO);
    color: white;
    text-align: center;
    font-family: epilogue;
    padding: 40px;
    display: flex;
    flex-direction: column;
    gap: 10px;
  }
 

  .footer h4 {
    font-family: epilogue;
    font-weight: 300;
    font-size: 0.8em;
    color: var(--colorC);
    text-align: center;
  }
  
  .wrapper-contact {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 20px;
  }
  .contact {
    text-decoration: none;
    color: var(--colorC);
    font-size: 1.3em;
    font-family: kanit;
    width: 100%;
    transform: rotate(0deg);
    transition: 0.2s ease-in-out;
  }
  .contact:hover {
    animation: bounce 0.4s ease-in-out;
  }

  a {
    color: rgb(100, 100, 229);
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
</style>
