<script>
  export let title;
  export let p;
  export let img;
  export let alt;
  export let job;
</script>

<!-- <div class="wrapper-cards"> -->
  <div class="card linear-gradient">
    <img src={img} {alt} class="img" />
    <h3>{title}</h3>
    <h4>{job}</h4>
    <h5><span>"</span>  {p}  <span>"</span> </h5>
  </div>
<!-- </div> -->

<style>
  /* .wrapper-cards {
    display: flex;
    width: auto;
  } */
  .card {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
    gap: 15px;
    width: calc(30.33% - 10px);
    height: calc(50.33% - 10px);
    font-family: epilogue;
    background-color: transparent;
    box-shadow:
      14px 16px 30px rgba(1, 6, 27, 0.376),
      -14px -16px 30px rgba(1, 6, 27, 0.392);
    padding: 30px;
    margin-bottom: 20px;
  }
  .linear-gradient {
    border-style: solid;
    border-width: 3px;
    border-image: linear-gradient(45deg, rgb(143, 55, 0), rgb(66, 228, 250)) 1;
  }
  .card h3 {
    font-size: 1.3em;
    color: var(--colorC);
    font-weight: 700;
    font-family: kanit;
    text-align: center;
  }
  .card h5 {
    font-size: 1em;
    color: var(--colorC);
    font-weight: 300;
    text-align: center;
    line-height: 30px;
    padding: 5px;
  }
  .card h5 span{
    font-size: 2em;
    font-family: 'Times New Roman', Times, serif;
  }
  .img {
    width: 130px;
    height: 130px;
    /* object-fit: cover; */

  }
  .card h4 {
    font-size: 0.8em;
    color: white;
    text-align: center;
  }

@media screen and (max-width:768px){
  .card{
    width: 80%;
    height: auto;
  }
}
</style>
