<script>
  import { Link } from "svelte-navigator";
  import NavBar from "../components/navbar.svelte";
</script>

<div class="container">
  <NavBar />
  <main>
    <div>
      <h1>404</h1>
      <h1>Page not Found</h1>
    </div>
  </main>
</div>

<style>
  .container {
    max-width: 900px;
    display: flex;
    justify-content: center;
  }

  main {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 1em;
    margin: 0 auto;
    text-align: center;
  }

  h1 {
    font-weight: 700;
    font-size: 36px;
  }

  main > div {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  @media (min-width: 900px) {
    h1 {
      font-size: 48px;
    }
  }

  @media (min-width: 600px) {
    main {
      max-width: none;
    }
  }
</style>
