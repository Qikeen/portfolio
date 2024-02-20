<script>
</script>

<style>
		
	.flex{
		width:100%;
		display:flex;
		justify-content: space-around;
		align-items: center;
		flex-wrap: wrap-reverse;
		background-color: var(--bg-color, slategray);
		
	}




	.flex :global(.content){
		padding:2vw;
		flex:2 0 50%;
	}

	.flex :global(.content) :global(p){
		color:var(--text-color, white);
		font-family: 'Red Hat Display', sans-serif;
		font-size: clamp(1.2rem,1.6vw,45px);;
		text-align:center;
	}

</style>
	
	<div class="flex"> 
		<slot />
	</div>