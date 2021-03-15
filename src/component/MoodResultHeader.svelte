<script>
  import MoodResultText from "./MoodResultText.svelte";
  import CircularProfilePic from "./CircularProfilePic.svelte";
  export let mood, imageURL;
</script>

<!-- <div class="tan d-flex justify-content-center align-items-center text-center"> -->

<CircularProfilePic {imageURL} />
<MoodResultText {...mood} />

<!-- </div> -->
<style>
</style>
