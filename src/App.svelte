<script>
  //   export let name;
  let firstName = "Rodri";
  let lastName = "Moura";
  let beltColour = "black";
  $: fullName = `${firstName} ${lastName}`;
  //   $: console.log(beltColour);
  $: {
    console.log(beltColour);
    console.log(fullName);
  }

  const handleClick = () => {
    beltColour = "orange";
  };

  const handleInput = e => {
    beltColour = e.target.value;
  };
</script>

<style>
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

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<main>
  <!-- <h1>Hello {name}!</h1> -->
  <!-- <p style="color: {beltColour}">{beltColour} belt</p> -->
  <!-- <button on:click={handleClick}>Update Belt colour</button> -->
  <!-- <input
    type="text"
    name="colour"
    id="colour"
    on:input={handleInput}
    value={beltColour} /> -->
  <!-- enlace de dos vias entre el input y la variable opvion larga-->
  <!-- opcion corta -->
  <!-- <input type="text" bind:value={beltColour} /> -->

  <p>{firstName} {lastName} - {beltColour} belt</p>
  <input type="text" bind:value={firstName} />
  <input type="text" bind:value={lastName} />
  <input type="text" bind:value={beltColour} />
</main>
