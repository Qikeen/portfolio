
<style>
	header{
		width:100%;
		height: 65ox;
		background: rgb(212,230,233);
		background: linear-gradient(180deg, rgba(230,233,233,1) 0%, rgba(240,245,245,1) 33%, rgba(252,252,252,1) 75%, rgba(245,245,245,1) 100%);
		border-bottom: 2px solid rgba(244,244,244,1);
		border-bottom-right-radius: 10px;
		border-bottom-left-radius: 10px;

	}
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
	.nostyle, .nostyle:hover, .nostyle:visited, .nostyle:focus, .nostyle:active  {
	  text-decoration: none;
	  color: inherit;
 	  outline: 0;
	  
	}

	h1{
		font-family:"East Sea Dokdo", sans-serif;
		font-size: clamp(2px,6vw,55px);

	}

	img{
		width:clamp(7vw,7vw,36px);
		height: auto;
		max-width: 36px;

	}
	ul>*{
		padding-left:5px;
		padding-right:5px;
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
	import logo from "$lib/images/logo-ph.png";
</script>

	<header class="flex"> 
		<div class="flex flex-item flex-center" style="justify-content: flex-start;">
			<a href="/" class="nostyle">
				<img src={logo} 
				style="padding: 5px;"
				width=36px height=36px>
				</a>
			<a href="/" class="nostyle"><h1 style="font-size: clamp(2px,8vw,55px);">Rainn.ee</h1></a>
		</div>
		<!--blank div for spacing -->
		<div class="flex-item"></div>
		<ul class="flex flex-item flex-center" style="padding:5px; justify-content: space-between;">
		
			<div><h1><a href="/about">About</a></h1></div>
			<div><h1><a href="/contact">Contact</a></h1></div>
			<div><h1><a href="/projects">Projects</a></h1></div>
			<div><h1><a href="/resume">Resume</a></h1></div>
			<div><!--another blank div for spacing (these are really useful in flexbox)--></div>
		</ul>
	</header>