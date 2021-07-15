
<!-- Svelte components are split into three parts:
- script
- style
- main html
 -->
 
<script>
	export let name;
	let paraphcss = "paraphcss";
</script>

<style>
  main {
    width: 80%;
    max-width: 800px;
    margin: 20px auto;
    padding: 20px;
  }

  label {
    font-weight: bold;
  }

  input {
    width: 80%;
  }
  
  
  .paraphcss {
	font-size: 120%;
	color: red;
  }
</style>

<main>
  <form>
    <label for="username">Enter a GitHub username:</label>
    <input type="text" name="username" placeholder="jackfranklin" />
    <button type="submit">Load repositories</button>
  </form>
  
  <br/>
  <br/>
		<p class={paraphcss}>Some text</p>
  <br/>
  <h1>Hello {name}!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
</main>

