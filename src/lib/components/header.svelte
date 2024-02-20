
<style>
/* dynamic css styling for shy, headroom style header */
	.unhide{		
		height:80px;
		z-index: 100;
		position: fixed;
		translate: 0 ;
		transition: all 200ms ease-out;
	
	}

	.unhide:hover{
		translate: 0;

	}

	.dynamic{
		translate:0 -70px;

	}
	.unhide:hover > .hide{
		display:inline-block;
		margin-top: 0;
		translate: 0;
		
	}

	.hide{		
		transition: all 1s ease-in-out;
		translate: 0 -80px;
		z-index: 100;
		
	}

	.invisible{
		opacity: 0;
		transition: all 100ms ease-in-out;

	}

	.gone{
		opacity: 0;
		display:none;
	}


/* flex styling */
	.flex{
		display:flex;
		justify-content: space-between;
		align-items: flex-end;
		

	}

	.flex-center{
		align-items: center;
	}

	.flex-item{
		flex-grow: 1;
	}
	/* remove styling from logo anchor */
	.nostyle, .nostyle:hover, .nostyle:visited, a.nostyle:focus, a.nostyle:active  {
	  text-decoration: none;
	  color: inherit;
 	  outline: 0;
 	  text-shadow: none;
	  
	}

/* colors and fonts targeting tags directly */
	header{
		width:100vw;
		height: 65px;
		background: rgb(212,230,233);
		background: linear-gradient(180deg, rgba(230,233,233,1) 0%, rgba(240,245,245,1) 33%, rgba(252,252,252,1) 75%, rgba(245,245,245,1) 100%);
		border-bottom: 2px solid rgba(244,244,244,1);
		border-bottom-right-radius: 10px;
		border-bottom-left-radius: 10px;
	
	}

	img{
		width:clamp(7vw,7vw,36px);
		height: auto;
		max-width: 36px;

	}
	ul>*{
		padding-left:5px;
		padding-right:5px;
		font-family:"East Sea Dokdo", sans-serif;
		font-size: clamp(2px,6vw,55px);
	
	}
	a{
		text-decoration: none;
		color:inherit;
		outline: 0;
	
	}
	a:hover{
		color:rgba(60,50,80,1);
		text-shadow: silver 1px 0 10px;
	
	}

</style>

<script>
	//initialize variable values
	import logo from "$lib/images/logo-ph.png";
	let y = 0;
	let lastY = 0;
	let threshold = 5;
	let dy = 0;
	let lastDy = 0;

//hide or show the header on upwards scrollY 
	function getDelta(y){
		//record change between y and lastY as dy
		dy = lastY - y;
		//update lastY
		lastY = y
		
		//update dy if the change between y and lastY is greater than threshold
		if(Math.abs(dy) <= threshold){
			
			dy=lastDy			
			return(dy)
		}
		else{			
			lastDy=dy
			return(dy)		
		}
	}

	
//set value of dy to the output of getDelta any time the y value is changed
	$: dy = getDelta(y);
	




</script>

<!-- bind scrollY to the value of y -->
<svelte:window bind:scrollY='{y}' />

<!-- this is the shy header, reveals on hover and disappears when main header enters view -->

<div class="unhide" class:dynamic={dy<threshold}>
<div class:invisible={y<100} class:gone={y<65} class:hide={dy<threshold} >
	<header class="flex"> 
		<div class="flex flex-item flex-center" style="justify-content: flex-start;">
			<a href="/" class="nostyle">
				<img src={logo} 
				style="padding: 5px;"
				width=36px height=36px>
				</a>
			<a href="/" class="nostyle" style="font-size: clamp(2px,8vw,55px); font-family:'East Sea Dokdo', sans-serif;">Rainn.ee</a>
		</div>

		<div class="flex-item"> <!--blank div for spacing --> </div>

		<nav class="flex-item" style = "padding-right: 1vw;">
			<ul class="flex flex-item flex-center" style="padding:5px; justify-content: space-between;">
			
				<a href="/about">About</a>
				<a href="/contact">Contact</a>
				<a href="/projects">Projects</a>
				<a href="/resume">Resume</a>
			</ul>
		</nav>
	</header>
</div>
</div>

<!-- main header-->
	<header class="flex"> 
		<div class="flex flex-item flex-center" style="justify-content: flex-start;">
			<a href="/" class="nostyle">
				<img src={logo} 
				style="padding: 5px;"
				width=36px height=36px>
				</a>
			<a href="/" class="nostyle" style="font-size: clamp(2px,8vw,55px); font-family:'East Sea Dokdo', sans-serif;">Rainn.ee</a>
		</div>
		
		<div class="flex-item"><!--blank div for spacing --></div>
		<nav class="flex-item" style = "padding-right: 1vw;">	
			<ul class="flex flex-item flex-center" style="padding:5px; justify-content: space-between;">
			
				<a href="/about">About</a>
				<a href="/contact">Contact</a>
				<a href="/projects">Projects</a>
				<a href="/resume">Resume</a>
			</ul>
		</nav>
	</header>
