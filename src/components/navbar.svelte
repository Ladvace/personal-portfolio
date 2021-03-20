<script>
  import { link } from "svelte-navigator";
  import Logo from "../../public/logo.svg";
</script>

<nav class="NavBar">
  <a href="/" use:link>
    <Logo class="logo" width="30" />
  </a>
  <div class="buttons">
    <a class="button" href="/">Home</a>
    <a class="button" href="/projects">Projects</a>
    <a class="button" href="/about">About</a>
  </div>
</nav>

<style>
  :global(.logo) {
    cursor: pointer;
  }
  .NavBar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    height: 90px;
    max-width: 900px;
    box-sizing: border-box;
    padding: 20px;
  }
  .buttons {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .buttons .button {
    padding: 10px;
    cursor: pointer;
    transition: color 0.2s ease-in-out;
    text-decoration: none;
    color: white;
    line-height: 1.75;
  }
  .buttons .button:hover {
    color: #f3a712;
    padding: 10px;
    cursor: pointer;
  }

  @media (min-width: 900px) {
    .NavBar {
      padding: 20px 0 0 0;
      display: flex;
      justify-content: space-between;
      max-width: 900px;
    }
  }
</style>
