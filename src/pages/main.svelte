<script>
  import { Link } from "svelte-navigator";
  import { faCog } from "@fortawesome/free-solid-svg-icons";
  import { faGithub, faLinkedin } from "@fortawesome/free-brands-svg-icons";
  import Fa from "svelte-fa";
</script>

<div class="container">
  <main>
    <h1>Hi!✋ I'm Gianmarco a Front End 💻 based in Italy</h1>
    <div class="icons">
      <Fa class="icon" icon={faCog} />
      <Fa class="icon" icon={faGithub} />
      <Fa class="icon" icon={faLinkedin} />
    </div>
    <div class="cards">
      <Link to="projects">
        <div class="card">Projects</div>
      </Link>
      <Link to="about">
        <div class="card">About</div>
      </Link>
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
    height: 4rem;
    border-radius: 5px;
    transition: transform 0.2s ease-in-out, background 0.2s ease-in-out;
    /* box-shadow 0.2s ease-in-out; */
  }

  .card:hover {
    transform: scale(1.03);
    cursor: pointer;
    background: #24262d;
  }

  .cards {
    /* max-width: 1200px; */
    margin: 100px auto;
    display: grid;
    grid-gap: 1rem;
  }

  /* footer {
    font-size: 16px;
    font-weight: 400;
    padding: 30px 0;
    max-width: 900px;
    text-align: center;
    width: 100%;
  }

  footer span {
    color: #ff3e00;
  } */

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
