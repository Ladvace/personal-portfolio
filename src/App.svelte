<script>
  import { onMount, onDestroy } from "svelte";
  import { globalHistory } from "svelte-navigator/src/history";
  import { Router, Route } from "svelte-navigator";
  import NavBar from "./components/navbar.svelte";
  import Main from "./pages/main.svelte";
  import Projects from "./pages/projects.svelte";
  import About from "./pages/about.svelte";
  import NotFound from "./pages/notFound.svelte";
  import { currentPath } from "./store.js";

  $currentPath = window.location.pathname;
  let unsub;
  onMount(() => {
    unsub = globalHistory.listen(({ location, action }) => {
      $currentPath = location.pathname;
    });
  });
  onDestroy(() => {
    unsub();
  });
</script>

<!-- <main> -->
<Router>
  {#if $currentPath != "/"}
    <NavBar />
  {/if}
  <div class="container">
    <Route path="projects" component={Projects} />
    <Route path="about" component={About} />

    <Route path="/" exact component={Main} />
    <Route component={NotFound} />
  </div>
  <footer>Created by Me ❤️ with <span>Svelte</span></footer>
</Router>

<!-- </main> -->
<style>
  /* main {
    display: grid;
  } */
  .container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    max-width: 900px;
  }

  footer {
    /* position: absolute; */
    /* bottom: 0; */
    font-size: 16px;
    font-weight: 400;
    padding: 30px 0;
    max-width: 900px;
    text-align: center;
    width: 100%;
  }

  footer span {
    color: #ff3e00;
  }
</style>
