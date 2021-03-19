<script>
  import { Link } from "svelte-navigator";
</script>

<div class="container">
  <main>
    <h1>About</h1>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Blanditiis itaque
      consequuntur nostrum soluta harum corporis, dignissimos veritatis magni
      distinctio ad eveniet odio quae unde vel ullam nihil tempore quis
      doloremque?
    </p>
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

  @media (min-width: 900px) {
    main > h1 {
      font-size: 48px;
    }
  }

  @media (min-width: 600px) {
    main {
      max-width: none;
    }
  }
</style>
