<script>
  import { Router, Route, Link } from "svelte-navigator";
  import Main from "./pages/main.svelte";
</script>

<Router>
  <main>
    <Route path="/">
      <Main />
    </Route>

    <Route path="about">
      <h3>About</h3>
      <p>That's what it's all about!</p>
    </Route>
  </main>
</Router>

<style>
  main {
    display: flex;
    justify-content: center;
  }
</style>
