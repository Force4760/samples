<script>
  import Home from "./Home.svelte";
  import Router from "svelte-spa-router";
  import Paid from "./Paid.svelte";
  import Yt from "./yt.svelte";
  const routes = {
    "/": Home,
    "/paid": Paid,
    "/yt": Yt,
  };
</script>

<main><Router {routes} /></main>

<style>
  :global(body) {
    background: linear-gradient(-45deg, #527cee, #5b3ce7, #23a6d5, #23d5ab);
    background-size: 400% 400%;
    animation: gradient 15s ease infinite;
  }
  @keyframes gradient {
    0% {
      background-position: 0% 50%;
    }
    50% {
      background-position: 100% 50%;
    }
    100% {
      background-position: 0% 50%;
    }
  }
  main {
    text-align: center;
    padding: 1em;
    max-width: 80vw;
    margin: 0 auto;
  }

  @media (min-width: 640px) {
    main {
      max-width: 90vw;
    }
  }
</style>
