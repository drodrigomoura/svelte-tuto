<script>
  let name;
  let beltColour;
  let age;

  // let fighting = false;
  // let sneaking = false;
  // let running = false;
  let skills = [];
  const handleSubmit = () => {
    console.log(name, beltColour, age, skills);
  };
</script>

<style>

</style>

<form on:submit|preventDefault={handleSubmit}>
  <input type="text" placeholder="name" bind:value={name} />
  <!-- <input type="text" placeholder="belt colour" bind:value={beltColour} /> -->
  <input type="number" placeholder="age" bind:value={age} />
  <label>Skills:</label>
  <!-- <input type="checkbox" bind:checked={fighting}/>Fighting<br/>
  <input type="checkbox" bind:checked={sneaking}/>Sneaking<br/>
  <input type="checkbox" bind:checked={running}/>Running<br/> -->
  <input type="checkbox" bind:group={skills} value="fighting"/>Fighting<br/>
  <input type="checkbox" bind:group={skills} value="sneaking"/>Sneaking<br/>
  <input type="checkbox" bind:group={skills} value="running"/>Running<br/>

  <select bind:value={beltColour}>
    <option value="black">black</option>
    <option value="orange">orange</option>
    <option value="brown">brown</option>
    <option value="white">white</option>
  </select>
  <button>Add Person</button>
</form>
