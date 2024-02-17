<script>
	


	import logo from "$lib/images/logo-ph.png"
	
	export let items = [];
	export let head = 'ur mom'
</script>



<style>

	h2 { 
		font-family:"Protest Revolution", sans-serif;
		font-size: clamp(2rem,7vw,55px);
		padding: 2vh;
		margin-top: 5vh;

	}

	ul{
		display:flex;
		justify-content: space-around;
		align-items: center;
		padding:2vh;
	}
</style>




	<h2> {head}</h2>

		<ul class='' style="background-color: #e6d0ac;">

			{#each items as src, index (src)}
				<li><img src={src} height=auto width = 100vw></li>
			{/each}

			
		</ul>