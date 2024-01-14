<script>
  export let icon;
  export let p;
  export let title;
</script>

<div class="wrapper-list">
  <div class="wrapper-icon">
    <div class="icon">{icon}</div>
  </div>
  <div class="p"><span>{title}</span>{p}</div>
</div>

<style>
  .wrapper-list {
    display: flex;
    flex-direction: row;
    margin: 20px;
    font-family: epilogue;
    color: var(--bg);
    width: 100%;
  }
  .wrapper-icon{
        display: flex;
        justify-content: center;
        align-items: center;
  }
  .icon {
    height: 80px;
    width: 80px;
    font-size: 2.4em;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-right: 20px;
   background-color: var(--primary);
    box-shadow: 2px 3px 10px rgba(0, 0, 0, 0.355);
    border: solid white 2px
  }
  .p {
    font-size: 1.2em;
    font-family: epilogue;
    color: var(--bg);
    font-weight: 400;
    list-style: none;
    padding: 10px;
  }
  .p span {
    font-weight: 800;
    color: transparent;
    -webkit-background-image: linear-gradient(to left, var(--blue), var(--ca));
    background-image: linear-gradient(to left, var(--blue), var(--ca));
    -webkit-background-clip: text;
    background-clip: text;
  }
  @media screen and (max-width:768px){
    .wrapper-list{
      flex-direction: column;
      align-items: center;
      justify-content: center;
          margin: 0px;
    }
    .wrapper-icon{
      margin-bottom: 20px;
    }
  }
</style>
