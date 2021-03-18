<script>
  import { Link } from "svelte-navigator";
  import NavBar from "../components/navbar.svelte";
</script>

<div class="container">
  <NavBar />
  <main>
    <h1>Projects</h1>
    <div class="projects">
      <Link to="projects">
        <div class="project">Project 1</div>
      </Link>
      <Link to="about">
        <div class="project">Project 22</div>
      </Link>
      <Link to="about">
        <div class="project">Project 3</div>
      </Link>
      <Link to="about">
        <div class="project">Project 4</div>
      </Link>
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

  .project {
    font-weight: 700;
    border: 1px dashed transparent;
    display: flex;
    flex-direction: column;
    background-color: #1b1c22;
    color: white;
    padding: 1rem;
    height: 4rem;
    border-radius: 5px;
    transition: transform 0.3s ease-in-out, background 0.3s ease-in-out;
    /* box-shadow 0.3s ease-in-out; */
  }

  .project:hover {
    /* box-shadow: 0px 15px 37px -20px rgba(64, 67, 79, 1); */
    transform: scale(1.04);
    cursor: pointer;
    background: #24262d;
  }

  .projects {
    /* max-width: 1200px; */
    margin: 50px auto;
    display: grid;
    grid-gap: 1rem;
    grid-template-columns: 1fr;
  }

  footer span {
    color: #ff3e00;
  }

  @media (min-width: 900px) {
    main > h1 {
      font-size: 48px;
    }

    .projects {
      grid-template-columns: 1fr;
    }

    .projects .project {
      /* height: 100%; */
      min-height: 200px;
    }
  }

  @media (min-width: 600px) {
    main {
      max-width: none;
    }
    .projects {
      grid-template-columns: 1fr;
    }
  }
</style>
