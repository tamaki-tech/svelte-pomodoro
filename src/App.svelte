<script lang="ts">
  export let name: string;
</script>

<main>
  <h1>Hello {name}!</h1>
  <p>
    Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn
    how to build Svelte apps.
  </p>
</main>

<style lang="scss">
  $sp: 640px;

  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  // SmartPhone
  @media screen and (max-width: 480px) {
    main {
      background-color: aqua;
    }
  }

  // Tablet
  @media screen and (min-width: 481px) and (max-width: 1024px) {
    main {
      max-width: none;
      background-color: bisque;
    }
  }

  // PC
  @media screen and (min-width: 1025px) {
    main {
      max-width: none;
    }
  }
</style>
