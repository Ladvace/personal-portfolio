<script>
  import { link } from "svelte-navigator";
  import { faCog } from "@fortawesome/free-solid-svg-icons";
  import { faGithub, faLinkedin } from "@fortawesome/free-brands-svg-icons";
  import Fa from "svelte-fa";
</script>

<div class="container">
  <main>
    <h1>Hi!✋ I'm Gianmarco a Front End 💻 based in Italy</h1>
    <div class="icons">
      <Fa class="icon" icon={faCog} />
      <a href="https://github.com/Ladvace" target="_blank">
        <Fa class="icon" icon={faGithub} />
      </a>
      <a href="https://www.linkedin.com/in/ladvace/" target="_blank">
        <Fa class="icon" icon={faLinkedin} />
      </a>
    </div>
    <div class="cards">
      <a href="/projects" use:link>
        <div class="card">
          <h2>Projects</h2>
          <p>List of projects</p>
        </div>
      </a>
      <a href="/about" use:link>
        <div class="card">
          <h2>About</h2>
          <p>Somethings more about me</p>
        </div>
      </a>
    </div>
  </main>
</div>

<style>
  .container {
    max-width: 900px;
    display: flex;
    justify-content: center;
  }

  a {
    color: white;
    text-decoration: none;
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
    margin: 50px 0;
    cursor: pointer;
    font-size: 30px;
  }
  .icons :global(.icon) {
    cursor: pointer;
    transition: color 0.2s ease-in-out;
  }
  .icons :global(.icon):hover {
    color: #f3a712;
  }
  .card {
    font-weight: 700;
    border: 1px dashed transparent;
    display: flex;
    flex-direction: column;
    background-color: #1b1c22;
    color: white;
    padding: 1rem;
    border-radius: 5px;
    transition: transform 0.2s ease-in-out, background 0.2s ease-in-out;
    text-align: left;
  }

  .card h2 {
    margin: 0;
  }
  .card p {
    margin: 0;
    font-weight: 100;
  }

  .card:hover {
    border: 1px dashed white;
    transform: scale(1.03);
    cursor: pointer;
    background: #24262d;
  }

  .cards {
    margin: 100px auto;
    display: grid;
    grid-gap: 1rem;
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

    .card {
      display: flex;
      justify-content: center;
      align-items: center;
    }
    .cards .card {
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
