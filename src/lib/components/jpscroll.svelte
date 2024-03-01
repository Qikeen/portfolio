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
	.scrollbottom{
		
	}
	.scrolltop{
		position: relative;

	}

	.checkbox{
		position:absolute;
		z-index: 5;
		width:50px;
		margin-top: 24.645vw;
		margin-left: -25px;
		left:50%;
		text-align:center;
		

	}

	.smol{
		margin:auto;
		max-width: 83vw;
		background-color: #F3EAD8;
	}

	svg{
		margin:-0.75vw;
	}

</style>
<div class="checkbox"><input disabled={isPlaying} type="checkbox" bind:checked={isOpen} /></div>

<div class="scrolltop">

	
	<div class="center">
	<svg
   viewBox="0 370 1560 410"
   version="1.1"
   id="svg1"
   xml:space="preserve"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:svg="http://www.w3.org/2000/svg"><defs
     id="defs1" /><g
     id="layer1"> <path
   id="rect8"
   style="fill:#f3ead8;stroke:#000000;stroke-width:1.1264"
   d="M 141.34972,716.0451 H 1418.6501 v 63.39169 H 141.34972 Z" /><rect
   style="fill:#efd19f;fill-opacity:1;stroke:#000000;stroke-width:1.32859;stroke-dasharray:none;stroke-opacity:1"
   id="rect6"
   width="1176.1704"
   height="103.96361"
   x="191.91472"
   y="677.6142" /><path
   id="rect7"
   style="fill:#f3ead8;stroke:#000000;stroke-width:1.07611"
   d="M 203.80982,715.67636 H 1356.19 v 64.12917 H 203.80982 Z" /><ellipse
   style="fill:#eed4a3;fill-opacity:1;stroke:#000000;stroke-width:1.46032;stroke-dasharray:none;stroke-opacity:1"
   id="path5"
   cx="76.921349"
   cy="709.56616"
   rx="26.823154"
   ry="42.895714" /><ellipse
   style="fill:#eed4a3;fill-opacity:1;stroke:#000000;stroke-width:1.46032;stroke-dasharray:none;stroke-opacity:1"
   id="ellipse5"
   cx="1483.0785"
   cy="709.56622"
   rx="26.823154"
   ry="42.895714" /><rect
   style="fill:#eed4a3;fill-opacity:1;stroke:#000000;stroke-width:1.18743;stroke-dasharray:none;stroke-opacity:1"
   id="rect5"
   width="1404.9697"
   height="64.045113"
   x="77.51506"
   y="677.54364"
   ry="18.644089" /><rect
   style="fill:#eed4a3;fill-opacity:1;stroke:#000000;stroke-width:1.43039;stroke-dasharray:none;stroke-opacity:1"
   id="rect4"
   width="1346.7964"
   height="96.94944"
   x="106.60172"
   y="661.09143"
   ry="28.222822" /><rect
   style="fill:#98956a;fill-opacity:1;stroke:#000000;stroke-width:1.47259;stroke-dasharray:none;stroke-opacity:1"
   id="rect3"
   width="1290.5708"
   height="107.2317"
   x="134.71455"
   y="655.95032"
   ry="7.6920543" /><rect
   style="fill:#efd19f;fill-opacity:1;stroke:#000000;stroke-width:1.34917;stroke-dasharray:none;stroke-opacity:1"
   id="rect2"
   width="1176.1498"
   height="107.21115"
   x="191.92503"
   y="655.96063" /><rect
   style="fill:#cdc8a0;fill-opacity:1;stroke:#000000;stroke-width:1.39186;stroke-dasharray:none;stroke-opacity:1"
   id="rect1"
   width="1152.0643"
   height="107.31245"
   x="203.96776"
   y="655.90997" /><path
   style="fill:none;fill-opacity:1;stroke:#000000;stroke-width:2.62579;stroke-dasharray:none;stroke-opacity:1"
   d="M 208.22693,655.15836 776.44285,373.47091 1355.5791,655.15836"
   id="path7" /></g></svg>
</div>

</div>

<div class="smol" use:unroll={isOpen}>
	<slot />
	
</div>
<div class="scrollbottom">
	
<svg

   viewBox="0 370 1560 500"
   version="1.1"
   id="svg1"
   xml:space="preserve"
   xmlns:xlink="http://www.w3.org/1999/xlink"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:svg="http://www.w3.org/2000/svg"><defs
     id="defs1" /><g
     id="layer1" ><image
       width="980.56451"
       height="576.96979"
       preserveAspectRatio="none"
       style="image-rendering:optimizeSpeed"
       id="image1"
       x="-161.02304"
       y="-2.4935668"
       transform="rotate(90)" /><path
       id="rect8"
       style="fill:#f3ead8;stroke:#000000;stroke-width:1.1264"
       d="M 1418.6501,436.30679 H 141.34974 V 372.9151 H 1418.6501 Z" /><rect
       style="fill:#efd19f;fill-opacity:1;stroke:#000000;stroke-width:1.32859;stroke-dasharray:none;stroke-opacity:1"
       id="rect6"
       width="1176.1704"
       height="103.96361"
       x="-1368.0851"
       y="-476.9798"
       transform="scale(-1)" /><path
       id="rect7"
       style="fill:#f3ead8;stroke:#000000;stroke-width:1.07611"
       d="M 1356.1899,436.33193 H 203.8097 v -64.12917 h 1152.3802 z" /><ellipse
       style="fill:#eed4a3;fill-opacity:1;stroke:#000000;stroke-width:1.46032;stroke-dasharray:none;stroke-opacity:1"
       id="path5"
       cx="-1483.0785"
       cy="-442.78571"
       rx="26.823154"
       ry="42.895714"
       transform="scale(-1)" /><ellipse
       style="fill:#eed4a3;fill-opacity:1;stroke:#000000;stroke-width:1.46032;stroke-dasharray:none;stroke-opacity:1"
       id="ellipse5"
       cx="-76.921349"
       cy="-442.78564"
       rx="26.823154"
       ry="42.895714"
       transform="scale(-1)" /><rect
       style="fill:#eed4a3;fill-opacity:1;stroke:#000000;stroke-width:1.18743;stroke-dasharray:none;stroke-opacity:1"
       id="rect5"
       width="1404.9697"
       height="64.045113"
       x="-1482.4847"
       y="-474.80823"
       ry="18.644089"
       transform="scale(-1)" /><rect
       style="fill:#eed4a3;fill-opacity:1;stroke:#000000;stroke-width:1.43039;stroke-dasharray:none;stroke-opacity:1"
       id="rect4"
       width="1346.7964"
       height="96.94944"
       x="-1453.3981"
       y="-491.26044"
       ry="28.222822"
       transform="scale(-1)" /><rect
       style="fill:#98956a;fill-opacity:1;stroke:#000000;stroke-width:1.47259;stroke-dasharray:none;stroke-opacity:1"
       id="rect3"
       width="1290.5708"
       height="107.2317"
       x="-1425.2853"
       y="-496.40155"
       ry="7.6920543"
       transform="scale(-1)" /><rect
       style="fill:#efd19f;fill-opacity:1;stroke:#000000;stroke-width:1.34917;stroke-dasharray:none;stroke-opacity:1"
       id="rect2"
       width="1176.1498"
       height="107.21115"
       x="-1368.0747"
       y="-496.39124"
       transform="scale(-1)" /><rect
       style="fill:#cdc8a0;fill-opacity:1;stroke:#000000;stroke-width:1.39186;stroke-dasharray:none;stroke-opacity:1"
       id="rect1"
       width="1152.0643"
       height="107.31245"
       x="-1356.032"
       y="-496.44189"
       transform="scale(-1)" /></g></svg>


</div>