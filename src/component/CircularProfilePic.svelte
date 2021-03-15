<script>
  export let imageURL;
</script>

<img class="circular--portrait" src={imageURL} alt="profile_image" />

<style>
  /* .circular--portrait {
    position: relative;
    width: 30vh;
    height: 30vh;
    overflow: hidden;
  } */
  .circular--portrait {
    /* width: 100%; */
    border-radius: 50%;
    height: 40vh;
    object-fit: cover;
    object-position: center;
  }
</style>
