<script>
	export let head = 'it was me Dio'
	let isOpen = false
	let isPlaying = ''
	let duration = 1000

	

	
	export function unroll(node, isOpen) {
		let initialHeight = node.offsetHeight;
			node.style.height = isOpen ? 'auto' : 0;
			node.style.overflow = "hidden";

		return {
			update(isOpen) {
				duration = 1000
				duration += (node.childElementCount * 250)
				console.log(node.childElementCount)
				console.log(duration)
				isPlaying = 'disabled'
				setTimeout(() => {
					isPlaying = ''
					console.log(isPlaying)
				}
					, duration )

				let animation = node.animate(
					[
						{
							height: initialHeight + 'px',
							overflow: 'hidden'
						},
						{
							height: 0,
							overflow: 'hidden'
						}
					],
					{ duration: duration, fill: 'both',
					easing: 'ease-in-out' }
					
				);
				animation.pause();
				if (!isOpen) {
					animation.play();
				} else {
					animation.reverse();
				}
			}
		};
	}
		

</script>
<style>
	.parent{
		margin-top: 20px;
		text-align:center;
	}
	div {
		border: solid 1px #333;
		box-sizing: border-box;
	}
	h1 {
		padding: 10px;
		margin: 0;
	}
	.smol{
		margin:auto;
		max-width: 70vw;
	}
	.disabled{
		
	}

</style>

<div class="parent"><input disabled={isPlaying} type="checkbox" bind:checked={isOpen} /></div>
<div class="smol" use:unroll={isOpen}>
	<slot />
</div>

