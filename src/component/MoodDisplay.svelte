<script>
  import { onMount } from "svelte";
  import Loading from "./Loading.svelte";
  import { calculateMood } from "../utils/moodDetector";
  import FullBreakdown from "./FullBreakdown.svelte";
  import MoodResultHeader from "./MoodResultHeader.svelte";
  let blank_avatar = "blank_avatar.png";

  export let songs, profile;

  let finishedShuffeling = false;
  let mood = calculateMood(songs);

  // Initiate loading page with 2-ish second delay
  onMount(() => {
    setTimeout(() => {
      finishedShuffeling = true;
    }, 2400);
  });

  // Direct user to loading page
  console.log(profile.images[0].url ? profile.images[0].url : "no image");
</script>

{#if finishedShuffeling === false}
  <div>
    <Loading text={"Detecting your mood"} />
  </div>
{:else}
  <div class="moodDisplay-container">
    <MoodResultHeader
      {mood}
      imageURL={profile.images[0].url ? profile.images[0].url : blank_avatar}
    />
    <FullBreakdown {mood} />
  </div>
{/if}

<style>
  .moodDisplay-container {
    text-align: center;
  }
</style>
