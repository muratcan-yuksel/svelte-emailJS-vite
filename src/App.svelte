<script>

  import emailjs from "@emailjs/browser";
  const baseUrl = import.meta.env.VITE_API_BASE_URL
	let email = '';
	let to_name = '';
	let name = '';
	let message = '';
  const handleForm=()=>{
    emailjs.send(
       "your service id",
        "template id",
        {
          to_name: "Murat",
          from_name: name,
          message: message,
          from_email: email,
        },
       "public key"
      );
  }
</script>

<main>
<div class="app">
	<div class="wrapper">
    <h1 class="title">Using EmailJs with Svelte and vite</h1>
		<input bind:value={email}>
		<input bind:value={name}>
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