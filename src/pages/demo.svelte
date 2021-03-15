<script>
  import { onMount } from "svelte";
  import {
    getRecentlyPlayedTracks,
    getSongAnalysisArray,
    getUserProfile,
  } from "../utils/functions";
  import AnalyzingContainer from "../component/AnalyzingContainer.svelte";
  import Loading from "../component/Loading.svelte";
  import { demoSongData, demoUserProfile } from "../utils/demoSongData";

  let finishedLoading = false;
  onMount(() => {
    setTimeout(() => {
      finishedLoading = true;
    }, 3000);
  });
</script>

<div class="demo-container">
  {#if finishedLoading === false}
    <Loading text={"Connecting To Spotify"} />
  {:else}
    <AnalyzingContainer songs={demoSongData} profile={demoUserProfile} />
  {/if}
</div>

<style>
  .demo-container {
    /* display: flex;
    align-items: center;
    justify-content: space-evenly;
    flex-direction: column; */
    height: 70vh;
    width: 100%;
  }
</style>
