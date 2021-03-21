<script>
  import { onMount, onDestroy } from "svelte";
  import { globalHistory } from "svelte-navigator/src/history";
  import { Router, Route, link } from "svelte-navigator";
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

<Router>
  {#if $currentPath != "/"}
    <NavBar />
  {/if}
  <div class="container">
    <Route path="projects" component={Projects} />
    <Route path="about" component={About} />

    <Route path="/" component={Main} />
    <Route component={NotFound} />
  </div>
  <footer>
    Created by <a class="me" href="about" use:link>Me</a> ❤️ with
    <span class="svelte">Svelte</span>
  </footer>
</Router>

<style>
  .container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    max-width: 900px;
  }

  footer {
    font-size: 16px;
    font-weight: 400;
    padding: 10px 0;
    max-width: 900px;
    text-align: center;
    width: 100%;
  }

  footer .svelte {
    color: #ff3e00;
  }

  a {
    text-decoration: none;
    color: #f3a712;
  }
</style>
