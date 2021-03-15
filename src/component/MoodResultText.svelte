<script>
  export let name, firstMood, secondMood, conjuction;
</script>

<div class="tan text-container">
  <h1 class="title-small">{name}</h1>
  <p class="bold fixed-container">
    Your recent songs have <span class="pinkish large-text">
      {firstMood.difference.toFixed(2)}%</span
    >
    {firstMood.mood.replace("-", " ")}
    {conjuction}
    <span class="pinkish large-text"> {secondMood.difference.toFixed(2)}%</span>
    {secondMood.mood.replace("-", " ")} than average.
  </p>
</div>

<style>
  .large-text {
    font-size: 25px;
  }
  .title-small {
    font-family: Poppins;
    font-style: normal;
    font-weight: bold;
    font-size: 50px;
    color: #ee7070;
    text-shadow: -4px 4px 0px #000000;
    line-height: 1.1;
  }
  .fixed-container {
    max-width: 30em;
    line-height: 35px;
  }
  .text-container {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }
</style>
