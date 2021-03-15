<script>
  import { useNavigate } from "svelte-navigator";

  const navigate = useNavigate();
  const {
    REACT_APP_SPOTIFY_CLIENT_ID,
    REACT_APP_SPOTIFY_AUTHORIZE_URL,
    REACT_APP_SPOTIFY_REDIRECT_URL,
  } = __myapp.env;

  const scopes = "user-read-private user-read-recently-played";
  const encodedScopes = encodeURIComponent(scopes);

  const handleLogin = () => {
    window.location = `${REACT_APP_SPOTIFY_AUTHORIZE_URL}?client_id=${REACT_APP_SPOTIFY_CLIENT_ID}&scope=${encodedScopes}&redirect_uri=${REACT_APP_SPOTIFY_REDIRECT_URL}&response_type=token&show_dialog=true`;
  };

  const handleDemoLogin = () => {
    navigate("demo");
  };
</script>

<div class="main-container">
  <div class="main-desc-container">
    <h1 class="title-medium">mood ring</h1>
    <h2 class="bold">How are you?</h2>
    <h3>A mood detector based on your recently played music.</h3>
    <div>
      <button class="btn-green" on:click={handleLogin}>
        Connect with Spotify
      </button>
    </div>
    <p>— Don't have a Spotify account? —</p>
    <div>
      <button class="btn-grey" on:click={handleDemoLogin}> View A Demo </button>
    </div>
  </div>
</div>

<style>
  .main-desc-container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-direction: column;
    height: 70vh;
    width: 100%;
  }
  .title-medium {
    font-family: Poppins;
    font-style: normal;
    font-weight: bold;
    font-size: 5rem;
    color: #ee7070;
    text-shadow: -4px 4px 0px #000000;
  }
  .btn-green {
    background-color: #1db954;
    font-size: 14px;
    width: 311px;
    color: white;
    line-height: 1;
    border-radius: 500px;
    padding: 16px 48px 18px;
    transition-property: background-color, border-color, color, box-shadow,
      filter;
    transition-duration: 0.3s;
    border-width: 0;
    letter-spacing: 2px;
    min-width: 160px;
    text-transform: uppercase;
    white-space: normal;
    display: inline-block;
    margin-bottom: 0;
    font-weight: 700;
    text-align: center;
    vertical-align: middle;
    touch-action: manipulation;
    cursor: pointer;
    background-image: none;
    border: 1px solid transparent;
  }

  .btn-green:hover {
    background-color: #1ed760;
  }

  .btn-grey {
    background-color: #fcea9a !important;
    font-size: 14px;
    /* color: white; */
    line-height: 1;
    border-radius: 500px;
    width: 310px;
    border-color: black;
    border-width: 5px;
    border: black;
    border-style: solid;
    padding: 16px 48px 18px;
    transition-property: background-color, border-color, color, box-shadow,
      filter;
    transition-duration: 0.3s;
    letter-spacing: 2px;
    min-width: 160px;
    text-transform: uppercase;
    white-space: normal;
    display: inline-block;
    margin-bottom: 0;
    font-weight: 700;
    text-align: center;
    vertical-align: middle;
    touch-action: manipulation;
    cursor: pointer;
    background-image: none;
    /* border: 1px solid transparent; */
  }

  .btn-grey:hover {
    background-color: #ee7070 !important;
  }
</style>
