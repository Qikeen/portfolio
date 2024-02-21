<script>
	import { pageTitle } from '../stores.js';
	pageTitle.set('Resume');
	import { Section } from '$lib'
	import { Slides } from '$lib'

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

</script>

	<style>
	h2{
		font-family:"East Sea Dokdo", sans-serif;
		font-size: clamp(2rem,7vw,55px);
		text-align: center;
		padding: 1vw;
		color: white;
	}
</style>




<Section>
	<div class="content">
		<p>
		Dependable and competent full-stack web developer with experience in graphic design and animation. 
		</p>
	</div>
</Section>

<Section --bg-color=aquamarine --text-color=black>
	<div class="content">
		<p>
		I utilize my experience in graphic design and animation, combined with the diverse technologies of web development to create unique and dynamic user experiences
		</p>
	</div>
</Section>

<Section>
	<div class="content" style=" flex:1 0 300px; align-self: stretch;">
		<h2>Education</h2>
		<p style="text-align: left; font-size:clamp(1.2rem, 1vw, 2vw);">
		Current &bull; MOOC - Cyber Security Base &bull; <b> University of Helsinki </b>
		<hr  />
		<p style="text-align: left; font-size:clamp(1.2rem, 1vw, 2vw);">
		2022-2023 &bull; Multimedia Technology - Animator Level II  &bull; <b> Dallas College </b>
		<hr />
		<p style="text-align: left; font-size:clamp(1.2rem, 1vw, 2vw);">
		2019-2021 &bull; 2.5 Years of study towards BA in Arts, Technology and Emerging Communication   &bull; <b> University of Texas at Dallas </b>
		<hr />
		<p style="text-align: left; font-size:clamp(1.2rem, 1vw, 2vw);">
		2019 &bull; AA Graphic Design & Digital Illustration  &bull; <b> Richland College </b>
		<hr />
		
	</div>
	<div class="content" style="flex:1 0 300px; align-self: stretch;">
		<h2>Work</h2>
		<p style="text-align: left; font-size:clamp(1.2rem, 1vw, 2vw);">
		Current &bull; Freelance Web Designer (Looking for work lol) 
		<hr />
		
		<p style="text-align: left; font-size:clamp(1.2rem, 1vw, 2vw);">
		2022 - 2023 &bull; Game Technician & Karaoke DJ &bull; <b> Two Bit Circus Dallas </b>
		<hr />
		<p style="text-align: left; font-size:clamp(1.2rem, 1vw, 2vw);">
		2021 &bull; Full-Time Student &bull; <b> University of Texas at Dallas </b>
		<hr />
		<p style="text-align: left; font-size:clamp(1.2rem, 1vw, 2vw);">
		2020 &bull;Technical Support & Teaching Assistant  &bull; <b> Country Club Active Learning </b>
		<hr />
	</div>
</Section>

<Slides --bg-color='aquamarine' items={items1} head="Skills" />
	<Slides --bg-color='aquamarine' items={items2} head=""  />




