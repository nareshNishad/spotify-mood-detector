<script>
  export let label, percent;
</script>

<h4 class="bold floating pinkish">{percent}</h4>
<h4 class="bold pinkish ">{label}</h4>

<style>
  .floating {
    animation-name: floating;
    animation-duration: 3s;
    animation-iteration-count: infinite;
    animation-timing-function: ease-in-out;
    font-size: 5rem;
    margin: 20px;
  }

  @keyframes floating {
    0% {
      transform: translate(0, 0px);
    }
    50% {
      transform: translate(0, 15px);
    }
    100% {
      transform: translate(0, -0px);
    }
  }
</style>
