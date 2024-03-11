<script>
  export let text;
  export let img;
  export let description;
</script>

<div class="card-services">
  <div class="wrapper-text">
    <div class="text-services">{text}</div>
    <p class="description-services">{description}</p>
  </div>
  <img src={img} alt="" class="img-services" />
</div>

<style>
  .card-services {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 20px;
    min-width: 300px;
    max-height: 600px;
    /* box-shadow: 0px 0px 10px 2px rgba(76, 76, 76, 0.35); */
    background-color: white;
    overflow: hidden;
    padding: 20px;
  }
  .wrapper-text {
    display: flex;
    flex-direction: column;
    align-items: first baseline;
    justify-content: first baseline;
    align-items: center;
    padding: 20px;
  }
  .text-services {
    font-family: epilogue;
    font-weight: 700;
    color: var(--primary);
    font-size: var(--l);
    text-align: left;
    padding: 20px;
    letter-spacing: -0.050em;
  }
  .description-services{
    font-family: poppins;
    font-weight: 400;
    color: grey;
    font-size: var(--m);
    text-align: left;
    letter-spacing: -0.00em;
  }
  .img-services {
    max-width: 400px;
    min-height: 300px;
    background-color: var(--CTA);
    object-fit: 100%;
    object-position: center;
       border-radius: 10px;
  }

  @media screen and (max-width: 768px) {
    .card-services {
      width: 220px;
      min-height: 650px;
    }
  }
</style>
