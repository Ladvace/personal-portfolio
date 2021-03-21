<script>
</script>

<div class="container">
  <main>
    <div>
      <h1>404</h1>
      <h3>Page not Found</h3>
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
    min-height: 500px;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 1em;
    margin: 0 auto;
    text-align: center;
  }

  h1 {
    margin: 0;
    font-weight: 700;
    font-size: 36px;
  }

  main > div {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
  }

  @media (min-width: 900px) {
    main {
      min-height: calc(100vh - 48px - 90px);
    }
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
