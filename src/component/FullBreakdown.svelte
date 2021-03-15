<script>
  import AddDisplayWhite from "./AddDisplayWhite.svelte";
  import AddDisplayPink from "./AddDisplayPink.svelte";
  import { fixCapitalization } from "../utils/functions";
  export let mood;
</script>

<div class="breakdown-container black-body">
  <div class="black-body">
    <h2 class="bold tan-font whiteish">Your Full Breakdown</h2>
    <AddDisplayWhite
      label={fixCapitalization(mood.firstMood.mood)}
      percent={mood.firstMood.difference.toFixed(2) + "%"}
    />
    <AddDisplayPink
      label={fixCapitalization(mood.secondMood.mood)}
      percent={mood.secondMood.difference.toFixed(2) + "%"}
    />
    <AddDisplayWhite
      label={fixCapitalization(mood.thirdMood.mood)}
      percent={mood.thirdMood.difference.toFixed(2) + "%"}
    />
    <AddDisplayPink
      label={fixCapitalization(mood.acousticnessDifference.mood)}
      percent={mood.acousticnessDifference.difference.toFixed(2) + "%"}
    />
    <AddDisplayWhite label={"Average Key"} percent={mood.key} />
    <AddDisplayPink label={"Average Tempo"} percent={mood.tempo} />
  </div>
</div>

<style>
  .breakdown-container {
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .whiteish {
    color: #e5e5e5;
  }
</style>
