<script>
  export let type;
  export let description;
  export let img;
  export let alt;
  // export let delai;
  // export let tarif;
</script>

<div class="card">
  <img src={img} {alt} class="img-card" />
  <div class="wrapper-text">
    <h2>{type}</h2>
    <p>{description}</p>
    
    <!-- <h4>{delai}</h4>
                <h5>{tarif}</h5> -->
  </div>
</div>

<style>
  .card {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 15px;
    max-width: 450px;
    min-height: 700px;
    font-family: epilogue;
    background-color: transparent;
    margin-top: 30px;
    margin-bottom: 20px;
    flex-shrink: 0;
    box-shadow: 0px 0px 10px 2px rgba(76, 76, 76, 0.35);
    background-color: var(--primary);
    /* background: linear-gradient(to top, rgba(255, 166, 0, 0.506), rgba(0, 0, 128, 0.434)); */
  }
  .wrapper-text {
    display: flex;
    flex-direction: column;
    align-items: first baseline;
    justify-content: first baseline;
    padding: 30px;
    gap: 30px;
  }
  .wrapper-text h2 {
    font-size: var(--l);
    color: white;
    font-weight: 700;
    font-family: epilogue;
    text-align: left;
    letter-spacing: -2px;
  }
  .wrapper-text p {
    font-family: poppins;
    font-size: var(--m);
    color: rgb(225, 223, 223);
    font-weight: 400;
    text-align: left;
    line-height: 30px;
    padding: 20px;
    border: none;
    border-radius: 20px;
    z-index: 2;
  }
  .img-card {
    margin-top: 50px;
    max-width: 500px;
    max-height: 150px;
    object-fit: 100%;
    border-radius: 10px;
  }
  /* .wrapper-text h4 {
    font-family: epilogue;
    font-size: var(--m);
    color: var--(primary);
    text-align: left;
    font-weight: 500;
    line-height: 30px;
    letter-spacing: -1px;

    border-radius: 10px;
    padding: 10px;
    box-shadow: 0px 0px 10px 2px rgba(76, 76, 76, 0.35);
  }
  .wrapper-text h5 {
    font-family: epilogue;
    font-size: var(--m);
    color: var--(primary);
    text-align: left;
    font-weight: 500;
    line-height: 30px;
    letter-spacing: -1px;
    background-color: rgba(255, 255, 255, 0.319);
    border-radius: 10px;
    padding: 10px;
    box-shadow: 0px 0px 10px 2px rgba(76, 76, 76, 0.35);
  } */

  @media screen and (max-width: 768px) {
    .card {
      width: 300px;
      min-height: 850px;
    }
    .wrapper-text h2 {
      font-size: var(--m);
    }
    .wrapper-text p {
      font-size: var(--s);
    }
    .img-card {
    margin-top: 50px;
    max-width: 500px;
    max-height: 100px;
    object-fit: 100%;
    border-radius: 10px;
  }
  }
</style>
