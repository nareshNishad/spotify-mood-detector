<script>
  import { fixDate, formatStr } from "../utils/functions";
  export let name, album, artist, imageURL, playedAt, countIndex;
</script>

<div class="tan analyzing-container">
  <div>
    <h2 class="bold ">
      Analyzing <span class="tan pinkish review-number bold"
        >{countIndex}/20</span
      >
    </h2>
    <div>
      <img class="album-cover" src={imageURL} alt="name" />
    </div>
    <h2 class="bold ">{formatStr(name)}</h2>
    <h3>{formatStr(artist)}</h3>
    <h4>{formatStr(album)}</h4>
    <h4 class="pinkish">{fixDate(playedAt)}</h4>
  </div>
</div>

<style>
  .analyzing-container {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .album-cover {
    position: cover;
    width: 40vh;
    height: 40vh;
  }
  .content-body {
    min-height: 92.5vh;
  }
</style>
