<script>

</script>

<nav class="navbar navbar-expand-lg bg-custom ">
  <div class="container-fluid ">
    <a class="navbar-brand text-white" href="/">Gralypho</a>
    <button class="navbar-toggler bg-toggle navbar-toggler-custom" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <a class="nav-link active text-white" aria-current="page" href="/">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link text-white" href="/">Features</a>
        </li>
        <li class="nav-item">
          <a class="nav-link text-white" href="/">Pricing</a>
        </li>
        <li class="nav-item">
          <!-- <a class="nav-link disabled text-white" aria-disabled="true">Disabled</a> -->
        </li>
      </ul>
    </div>
  </div>
</nav>



<style>
.bg-custom{
        background-color: var(--colorO);
        /* box-shadow: 0px 0px 10px 0px var(--colorL); */
        padding: 20px;
}
.bg-toggle{
        background-color: var(--colorA);
        border: none;
        transition: 0.3s ease-in-out;

}
.bg-toggle:hover{
    transform: scale(1.1);

}
.navbar-toggler-custom:focus {
  outline: none; /* Annule la bordure de focus */
  box-shadow: none; /* Annule l'ombre de focus */
  background-color: grey;

}

</style>