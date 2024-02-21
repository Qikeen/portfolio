<script>
	import { Section } from "$lib"
	import { pageTitle } from '../stores.js';
	pageTitle.set('Contact');
	let formName = 'contact'

</script>
<style>
	h1{
		font-family:"Protest Revolution", sans-serif;
		font-size: clamp(2rem,7vw,55px);
		text-align: center;
		padding: 5vh;
	}
	
	h2{
		font-family:"Red Hat Display", sans-serif;
		font-size: clamp(1.2rem,4vw,30px);
		text-align: center;
		color:white;

	}

	.flex-vertical{
		display: flex;
		flex-direction: column;
		margin: 5vh 10vw;
		border-radius: 1vw;
		align-items: center;
		background-color: slategray;
	}

	.flex-vertical > *{
		margin-left:1vw;
		margin-right:1vw;
		margin-top: 0.5vh;
		width:75%;

	}
	.flex-vertical > label{
		font-family: 'East Sea Dokdo', sans-serif;
		font-size: clamp(1rem,6vw,45px);
		margin-top: 2vh;
		color: white;
	}
	.flex-vertical > .button{
		align-self: flex-end;
		margin: 2vw;
		margin-bottom: 1vw;
		max-width: 100px;
	}

	.flex-vertical > h2{
		font-family: 'East Sea Dokdo', sans-serif;
		font-size: clamp(1.2rem,6vw,60px);
	}

	.flex-vertical > textarea{
		font-size: 0.8rem;
		resize: vertical;
	}

</style>

<h1>Contact</h1>

<Section>
	<div class='content' style="flex:0 2 22%">
		<hr />
		<h2>Front-End Development</h2>
		<hr />
		<p>Front-end development and UI/UX design for websites and applications
		</p>
		<hr />
	</div>
	<div class='content' style="flex:0 2 22%;">
		<hr />
		<h2>Back-End Development</h2>
		<hr />
		<p>Back-end development and database services using PhP, SQL and jQuery for web-based applications
		</p>
		<hr />
	</div>
	<div class='content' style="flex:0 2 22%;">
		<hr />
		<h2>Graphic Design/ Digital Illustration</h2>
		<hr />
		<p>Graphic design and digital illustration services for any industry.
		</p>
		<hr />
	</div>
</Section>

<form  class="flex-vertical" name={formName} method="POST" netlify-honeypot="bot-field" data-netlify="true">
<input type="hidden" name="form-name" value={formName} />

	<h2>Leave Me A Message</h2>
 
	<label for="name">Name</label>
	<input name="name" id="name" required placeholder="Name" type="text" />
 	<label for="email">Email</label>
 	<input name="email" id="email" required placeholder="Email" type="email" />
 	<label for="message">Message</label>
 	<textarea name="message" id="message" placeholder="Message" rows=10 required type="text"></textarea>
 	<input class="button" type="submit" value="Submit" />
</form>
