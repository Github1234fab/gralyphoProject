<script>
  import { onMount } from "svelte";

  let Year;

  onMount(() => {
    Year = new Date().getFullYear();
  });
</script>

<footer class="footer">
  <h1>Gralypho</h1>
  <div class="wrapper-contact">
 <a href="mailto:gralypho@gmail.com " class="contact">gralypho@gmail.com</a>
<a href="tel:0672901614" class="contact">06 72 90 16 14</a>
  </div>

  <div class="wrapper-media">
    <a
      href="https://facebook.com/intent/tweet?url=URL_DU_SITE&text=Texte_du_tweet&via=NomUtilisateurTwitter"
      target="_blank"><i class="fa-brands fa-square-facebook anim"></i></a
    >
    <a
      href="https://twitter.com/intent/tweet?url=URL_DU_SITE&text=Texte_du_tweet&via=NomUtilisateurTwitter"
      target="_blank"><i class="fa-brands fa-square-twitter anim"></i></a
    >
    <a
      href="https://instagram.com/intent/tweet?url=URL_DU_SITE&text=Texte_du_tweet&via=NomUtilisateurTwitter"
      target="_blank"><i class="fa-brands fa-square-instagram anim"></i></a
    >
    <a
      href="https://tiktok.com/intent/tweet?url=URL_DU_SITE&text=Texte_du_tweet&via=NomUtilisateurTwitter"
      target="_blank"><i class="fa-brands fa-tiktok anim"></i></a
    >
  </div>
  <h4>© {Year} GRALYPHO. <br /> Tous droits réservés.</h4>
</footer>

<style>
  .footer {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: auto;
    height: 100%;
    font-size: 16px;
    background-color: var(--colorO);
    color: white;
    text-align: center;
    font-family: epilogue;
    padding: 40px;
    margin-top: 100px;
  }
  .footer h1 {
    grid-column: 6;
    grid-row: 1;
    font-weight: 800;
    font-size: 2.8em;
    color: transparent;
    font-family: kanit;
    -webkit-background-clip: text;
    background-clip: text;
     -webkit-background-image: linear-gradient(to right, var(--colorD), var(--colorI));
    background-image: linear-gradient(to right, var(--colorD), var(--colorI));
  }

  .footer h4 {
    grid-column: 1/12;
    grid-row: 4;
    font-family: epilogue;
    font-weight: 300;
    font-size: 0.8em;
    color: var(--colorC);
    text-align: center;
  }
  .wrapper-media {
    display: flex;
    grid-column: 6/10;
    grid-row: 3;
    gap: 30px;
    margin-bottom: 30px;
    margin-top: 30px;
    margin-left: 5px;

  }
  .wrapper-contact{
    grid-column: 1/12;
    grid-row: 2;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;



  }
  .contact {
    text-decoration: none;
    color:  var(--colorC);
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
