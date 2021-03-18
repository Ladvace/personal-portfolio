<script>
  import { faCog } from "@fortawesome/free-solid-svg-icons";
  import { faGithub, faLinkedin } from "@fortawesome/free-brands-svg-icons";
  import Fa from "svelte-fa";
</script>

<div class="container">
  <main>
    <h1>Hi!✋ I'm Gianmarco a Front End 💻 based in Italy</h1>
    <div class="icons">
      <Fa icon={faCog} />
      <Fa icon={faGithub} />
      <Fa icon={faLinkedin} />
    </div>
    <div class="cards">
      <div class="card">ONE</div>
      <div class="card">TWO</div>
      <div class="card">THREE</div>
      <div class="card">FOUR</div>
      <div class="card">FIVE</div>
      <div class="card">SIX</div>
    </div>
    <footer>Created by Me ❤️ with <span>Svelte</span></footer>
  </main>
</div>

<style>
  .container {
    max-width: 900px;
    display: flex;
    justify-content: center;
  }

  main {
    text-align: center;
    padding: 1em;
    margin: 0 auto;
    text-align: center;
  }

  h1 {
    font-weight: 700;
  }

  main > h1 {
    margin: 50px 0 0 0;
    font-size: 36px;
  }

  .icons {
    margin: 50px 0 0 0;
    cursor: pointer;
    font-size: 30px;
  }

  .card {
    border: 1px dashed transparent;
    display: flex;
    flex-direction: column;
    background-color: #1b1c22;
    color: white;
    padding: 1rem;
    height: 4rem;
    border-radius: 5px;
    transition: transform 0.5s;
  }

  .card:hover {
    transform: scale(1.05);
    cursor: pointer;
  }

  .cards {
    /* max-width: 1200px; */
    margin: 50px auto;
    display: grid;
    grid-gap: 1rem;
  }

  footer span {
    color: #ff3e00;
  }

  @media (min-width: 900px) {
    main > h1 {
      font-size: 48px;
    }

    .icons {
      font-size: 40px;
    }

    .cards {
      grid-template-columns: repeat(3, 1fr);
    }

    .cards .card {
      /* height: 100%; */
      min-height: 200px;
    }
  }

  @media (min-width: 600px) {
    main {
      max-width: none;
    }
    .cards {
      grid-template-columns: repeat(2, 1fr);
    }
  }
</style>
