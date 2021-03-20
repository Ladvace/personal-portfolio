<script>
  import { link } from "svelte-navigator";
  import Burger from "./hamburger.svelte";
  import Logo from "../../public/logo.svg";

  let opened = false;
  $: console.log(opened);
</script>

<nav class={opened ? "NavBar open" : "NavBar"}>
  <div class="innerContainer">
    <a href="/" use:link>
      <Logo class="logo" width="30" />
    </a>
    <div class="burger">
      <Burger bind:open={opened} />
    </div>
    <div class="buttons">
      <a class="button" href="/">Home</a>
      <a class="button" href="/projects">Projects</a>
      <a class="button" href="/about">About</a>
    </div>
  </div>
  <div class="responsiveButtons buttons">
    <a class="button" href="/">Home</a>
    <a class="button" href="/projects">Projects</a>
    <a class="button" href="/about">About</a>
  </div>
</nav>

<style>
  :global(.logo) {
    cursor: pointer;
  }

  .open {
    flex-direction: column !important;
    align-items: center !important;
    height: 250px !important;
    transition: height 0.2s cubic-bezier(0.455, 0.03, 0.515, 0.955);
  }

  .innerContainer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    max-width: 900px;
    box-sizing: border-box;
  }
  .innerContainer :global(a) {
    height: 30px;
  }

  .NavBar {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    max-width: 900px;
    box-sizing: border-box;
    padding: 20px;
    height: 90px;
    overflow: hidden;
    transition: height 0.2s cubic-bezier(0.455, 0.03, 0.515, 0.955);
  }

  .responsiveButtons {
    display: none !important;
    margin-top: 20px;
  }
  .buttons {
    display: none;
    justify-content: space-between;
    align-items: center;
  }

  .responsiveButtons {
    width: 100%;
    display: flex !important;
    flex-direction: column;
  }

  .responsiveButtons .button {
    width: 100%;
    text-align: center;
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

  .burger :global(button) {
    margin: 0;
  }
  @media (min-width: 900px) {
    .NavBar {
      padding: 20px 0 0 0;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      max-width: 900px;
    }

    .buttons {
      display: flex;
    }

    .NavBar .burger {
      display: none !important;
    }
    .responsiveButtons {
      display: none !important;
    }
  }
</style>
