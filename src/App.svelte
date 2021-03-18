<script>
  import { Router, Route } from "svelte-navigator";
  import Main from "./pages/main.svelte";
  import Projects from "./pages/projects.svelte";
  import NotFound from "./pages/notFound.svelte";
</script>

<Router>
  <div>
    <Route path="projects" component={Projects} />

    <Route path="about">
      <h3>About</h3>
    </Route>

    <Route path="/" exact component={Main} />
    <Route component={NotFound} />
  </div>
</Router>

<style>
  div {
    display: flex;
    justify-content: center;
  }
</style>
