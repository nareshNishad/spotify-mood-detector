<script>
  export let text;
</script>

<div class="loader-container">
  <div class="loader" role="status" />
  <h3 class="tan about-header">{text}</h3>
</div>

<style>
  .loader-container {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }
  .loader {
    border: 16px solid transparent;
    border-radius: 50%;
    border-top: 16px solid #ee7070;
    width: 60px;
    height: 60px;
    animation: spin 2s linear infinite;
  }
  .about-header {
    font-size: 40px;
  }

  @keyframes spin {
    0% {
      transform: rotate(0deg);
    }
    100% {
      transform: rotate(360deg);
    }
  }
</style>
