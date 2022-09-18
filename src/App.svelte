<script>
	let from_email = '';
	let to_name = '';
	let from_name = '';
	let message = '';
  const handleForm=()=>{
    console.log(from_email,to_name,from_name,message)
  }
</script>

<main>
<div class="app">
	<div class="wrapper">
    <h1 class="title">Using EmailJs with Svelte and vite</h1>
		<input bind:value={from_email}>
		<input bind:value={from_name}>
		<textarea name="" id="" cols="30" rows="10" bind:value={message}></textarea>
    <button class="btn" on:click={handleForm}>Send Email</button>
	</div>
</div>

</main>

<style>
	.app{
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
    background: rgb(7, 7, 56);
    color: whitesmoke;
	}
.wrapper{
	width: 40%;
	display: flex;
	flex-direction: column;
	/* border: solid; */
}
</style>