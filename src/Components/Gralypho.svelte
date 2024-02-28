<div class="rect">
  <div class="rec-left">G</div>
  <!-- <div class="rec-right"></div> -->
</div>

<style>
  .rect {
    display: flex;
    width: 130px;
    height: 40px;
    font-family: poppins;
    font-weight: 500;
    /* background-color: var(--bg); */
    /* padding: 5px; */
    justify-content: center;
    align-items: center;
    border-radius: 5px;
  }
  .rect:hover{
        animation: bounce 0.4s ease-in-out;
  }
  .rec-left {
    width: 50%;
    height: 45px;
    color: #6CA0DC;
    font-size: 1.8em;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: var(--bg);
    font-weight: 600;
    border-radius: 4px;
    border: solid 1px #6CA0DC;
  }
  .rec-right {
     display: flex;
    justify-content: center;
    align-items: center;
    width: 70%;
    background-color: var(--bg);
    text-align: center;
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
