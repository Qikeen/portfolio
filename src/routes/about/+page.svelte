<script>
	import { fade } from 'svelte/transition';
	import { onMount } from 'svelte';
	import { Slides } from '$lib'
	import { Footer } from '$lib'


	import { pageTitle } from '../stores.js';
	pageTitle.set('About');

	import logo from "$lib/images/logo-ph.png"
	import js from "$lib/images/js.svg"
	import css3 from "$lib/images/css3.svg"
	import html5 from "$lib/images/html5.svg"
	import svelte from "$lib/images/svelte.svg"
	
	let items1 = [js, css3, html5, svelte]


	import wp from "$lib/images/wp.png"
	import adobeCC from "$lib/images/adobeCC.png"
	import git from "$lib/images/github.png"
	import putty from "$lib/images/puTTY.png"

	let items2 = [wp, adobeCC, git, putty]


	let delay = 1000;

	let foo = false;

	onMount(() => {
	foo = true

});
	</script>

	<style>
	h1{
		font-family:"Protest Revolution", sans-serif;
		font-size: clamp(2rem,7vw,55px);
		text-align: center;
		padding: 5vh;
	}
	.flex{
		display:flex;
		justify-content: space-around;
		align-items: center;
	}

	.content{
		padding:3vh;
	}

	p{
		color:white;
		font-family: 'Red Hat Display', sans-serif;
		font-size: 1.2rem;
		text-align:center;
		padding-left: 10vw;
		padding-right: 10vw;
		min-width: 208px;
	}
	h2 { 
		font-family:"Protest Revolution", sans-serif;
		font-size: clamp(2rem,7vw,55px);
		padding: 2vh;
		margin-top: 5vh;

	}

</style>


<h1> About Me </h1>
	<div class="flex" style="background-color: slategray;"> 
		<div class="content">
			<p>
				 Mogul talk. It’s important to use cocoa butter. It’s the key to more success, why not live smooth? Why live rough? You see that bamboo behind me though, you see that bamboo? Ain’t nothin’ like bamboo. Bless up. You smart, you loyal, you a genius. Don’t ever play yourself. You should never complain, complaining is a weak emotion, you got life, we breathing, we blessed.
			</p>
			<p>
				 The key to more success is to get a massage once a week, very important, major key, cloth talk. It’s on you how you want to live your life. Everyone has a choice. I pick my choice, squeaky clean. The first of the month is coming, we have to get money, we have no choice. It cost money to eat and they don’t want you to eat. Another one. Major key, don’t fall for the trap, stay focused. It’s the ones closest to you that want to see you fail.
			</p>
			<p>
				 Every chance I get, I water the plants, Lion! Special cloth alert. A major key, never panic. Don’t panic, when it gets crazy and rough, don’t panic, stay calm. In life there will be road blocks but we will over come it. Another one. You see the hedges, how I got it shaped up? It’s important to shape up your hedges, it’s like getting a haircut, stay fresh. The key to more success is to have a lot of pillows. You should never complain, complaining is a weak emotion, you got life, we breathing, we blessed.
			</p>
			<p>
				 It’s on you how you want to live your life. Everyone has a choice. I pick my choice, squeaky clean. We don’t see them, we will never see them. They never said winning was easy. Some people can’t handle success, I can. We the best. Celebrate success right, the only way, apple. Let’s see what Chef Dee got that they don’t want us to eat. Mogul talk. To be successful you’ve got to work hard, to make history, simple, you’ve got to make it. We the best. Celebrate success right, the only way, apple.
			</p>
		</div>
	

		<img src={logo} height=auto width=100% style="min-width: 140px; padding-right: 2vw;">
	</div>
	<Slides  items={items1} head="Tools" />
	<Slides  items={items2} head="Programs"  />
	
	<Footer />
