<script lang="ts">
  import Button, { Label } from "@smui/button";
  import Slider from "@smui/slider";

  let value = 0;
</script>

<main>
  <h1 class="title">Svelte Pomodoro!</h1>
  <h1>00:00</h1>
  <p>
   This is a web timer app for pomodoro techniques with Svelte.js
  </p>
  <div>
    <Button variant="raised">
      <Label>Start</Label>
    </Button>
    <Button variant="raised">
      <Label>Stop</Label>
    </Button>
  </div>
  <br />
  <div>
    <h2>Work Time</h2>
    <Slider
      bind:value
      min={-10}
      max={10}
      step={2}
      discrete
      input$aria-label="Discrete slider"
    />
  </div>
  <div>
    <h2>Break Time</h2>
    <Slider
      bind:value
      min={-10}
      max={10}
      step={2}
      discrete
      input$aria-label="Discrete slider"
    />
  </div>

  <pre class="status">Value: {value}</pre>
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
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
    color: #ff3e00;
  }
  // SmartPhone
  @media screen and (max-width: 480px) {
    main {
      background-color: aqua;
    }
    h1 {
      font-size: 2.5em;
    }
  }

  // Tablet
  @media screen and (min-width: 481px) and (max-width: 1024px) {
    main {
      max-width: 480px;
      background-color: bisque;
    }
  }

  // PC
  @media screen and (min-width: 1025px) {
    main {
      max-width: 600px;
    }
  }
</style>
