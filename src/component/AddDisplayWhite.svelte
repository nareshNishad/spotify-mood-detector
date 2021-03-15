<script>
  export let label, percent;
</script>

<h4 class="bold floating-two whiteish">{percent}</h4>
<h4 class="bold whiteish mt-3 mb-5">{label}</h4>

<style>
  .floating-two {
    animation-name: floating;
    animation-duration: 4s;
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
  .whiteish {
    color: whitesmoke;
  }
</style>
