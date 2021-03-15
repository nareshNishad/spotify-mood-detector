<script>
  import { onMount } from "svelte";
  import AnalyzingDisplay from "./AnalyzingDisplay.svelte";
  import Loading from "./Loading.svelte";

  import MoodDisplay from "./MoodDisplay.svelte";

  let analyizedSong = "";
  let finishedShuffeling = false;
  export let songs, profile;
  console.log(profile);
  onMount(() => {
    songs.forEach((song, i) => {
      setTimeout(() => {
        analyizedSong = song;
      }, i * 150);
    });
    setTimeout(() => {
      finishedShuffeling = true;
    }, 3150);
  });
</script>

<!-- Return loading screen while waiting for async/await -->
{#if finishedShuffeling === false && songs.length === 0}
  <div>
    <Loading text={"Connecting with Spotify."} />
  </div>
  <!-- Return YourMood page when shuffeling is complete -->
{:else if finishedShuffeling === false && songs.length > 0}
  <AnalyzingDisplay {...analyizedSong} />
  <!-- Shuffle through songs being 'analyized' -->
{:else}
  <div>
    <MoodDisplay {songs} {profile} />
  </div>
{/if}
