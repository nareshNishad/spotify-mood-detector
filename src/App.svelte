<script>
  import { Router, Route, Link } from "svelte-navigator";
  import Home from "./pages/Home.svelte";
  import Navbar from "./component/Navbar.svelte";
  import Demo from "./pages/demo.svelte";
</script>

<Router>
  <Navbar />
  <Route path="demo">
    <Demo />
  </Route>
  <Route path="/test">
    <h2>tect</h2>
  </Route>
  <Route path="/">
    <Home />
  </Route>
</Router>
<svelte:head>
  <style>
    * {
      margin: 0;
      padding: 0;
      font-family: "Overpass", sans-serif;
      color: inherit;
      text-decoration: none;
      background-color: #fcea9a;
    }

    .tan {
      background-color: #fcea9a !important;
    }

    .tan > * {
      background-color: #fcea9a !important;
    }

    .tan > * > * {
      background-color: #fcea9a !important;
    }
    .bold {
      font-family: Poppins;
      font-style: normal;
      font-weight: bold;
      font-size: x-large;
    }

    .pinkish {
      color: #ee7070;
    }

    .black-body {
      background-color: black !important;
    }

    .black-body > * {
      background-color: black !important;
    }

    .white {
      color: #e5e5e5;
    }
  </style>
</svelte:head>
