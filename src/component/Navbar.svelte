<script>
  import { Link } from "svelte-navigator";
</script>

<nav class="container">
  <div class="brand-text">
    <Link to="/"><span class=" pinkish">mood ring</span> {"{"} beta {"}"}</Link>
  </div>
  <div class="brand-text">
    <Link to="/about">about</Link>
  </div>
</nav>

<style>
  :global(a) {
    font-weight: 700;
    font-size: x-large;
    text-decoration: none;
    color: #000 !important;
  }

  .container {
    margin: 10px 50px;
    display: flex;
    align-items: baseline;
    justify-content: space-between;
    margin-bottom: 10vh;
  }
  .pinkish {
    color: #ee7070;
  }
</style>
