<script>
	import { Slides } from "$lib"
	import { pageTitle } from '../stores.js';
	pageTitle.set('Contact');

	import js from "$lib/images/js.svg"
	import css3 from "$lib/images/css3.svg"
	import html5 from "$lib/images/html5.svg"
	import svelte from "$lib/images/svelte.svg"

	let items = [js, css3, html5, svelte]

</script>

<Slides {items} />

<h1>Contact</h1>
<a href="/"> go back </a>