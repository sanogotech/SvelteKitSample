
<!-- Svelte components are split into three parts:
- script
- style
- main html
 -->
 
<script>

	import Home from "./routes/Home.svelte";
	import About from "./routes/About.svelte";
	import Nested from './Nested.svelte';
	
	export let url = "";
	
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
  
  
  	p {
		color: purple;
		font-family: 'Comic Sans MS', cursive;
		font-size: 2em;
	}
</style>

<main>


  <nav>
    <a href="/">home</a>
    <a href="/about">about</a>
    <a href="/profile">profile</a>
    <a href="/news">news</a>
	
  </nav>



  <form>
    <label for="username">Enter a GitHub username:</label>
    <input type="text" name="username" placeholder="jackfranklin" />
    <button type="submit">Load repositories</button>
  </form>
  
  <br/>
  
	<p>These styles...</p>
  <Nested/>
  
  <br/>
		<p class={paraphcss}>Some text</p>
  <br/>
  <h1>Hello {name}!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
</main>

