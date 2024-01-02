<script>
</script>

<nav class="navbar navbar-expand-lg bg-custom">
  <div class="container-fluid">
    <a class="navbar-brand text-white" href="/">Gralypho</a>
    <button
      class="navbar-toggler bg-toggle navbar-toggler-custom"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarNav"
      aria-controls="navbarNav"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <a class="nav-link active text-white" aria-current="page" href="/#sectionF">Référencement</a>
        </li>
        <li class="nav-item">
          <a class="nav-link text-white" href="/#sectionC">Technologies</a>
        </li>
        <li class="nav-item">
          <a class="nav-link text-white" href="/">Tarifs</a>
        </li>
        <li class="nav-item">
          <!-- <a class="nav-link disabled text-white" aria-disabled="true">Disabled</a> -->
        </li>
      </ul>
    </div>
  </div>
</nav>

<style>
  .bg-custom {
    background-color: var(--colorO);
    /* box-shadow: 0px 0px 10px 0px var(--colorL); */
    padding: 20px;
  }
  .bg-toggle {
    background-color: rgb(100, 100, 229);
    border: none;
    transition: 0.3s ease-in-out;
  }
  .bg-toggle:hover {
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
  .navbar-toggler-custom:focus {
    outline: none; /* Annule la bordure de focus */
    box-shadow: none; /* Annule l'ombre de focus */
    background-color: grey;
  }
</style>
