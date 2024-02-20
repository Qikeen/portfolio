<script>
	import { Bio } from "$lib"
	import { pageTitle } from '../stores.js';
	pageTitle.set('Contact');

  let isSubmitting = false;

  const handleSubmit = (e) => {
    let myForm = document.getElementById("test");
    let formData = new FormData(myForm);
    isSubmitting = true;
    return fetch("/", {
      method: "POST",
      headers: { "Content-Type": "application/x-www-form-urlencoded" },
      body: new URLSearchParams(formData).toString(),
    })
      .then(() => {
        console.log("Form successfully submitted");
        isSubmitting = false;
        myForm.reset();
      })
      .catch((error) => {
        alert(error);
        isSubmitting = false;
      });
  };


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
</style>

<h1>Contact</h1>

<Bio>
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
		<h2>Graphic Design/Digital Illustration</h2>
		<hr />
		<p>Graphic design and digital illustration services for any industry.
		</p>
		<hr />
	</div>
</Bio>
<form
  id="test"
  name="test"
  on:submit|preventDefault={handleSubmit}
  netlify
  netlify-honeypot="bot-field"
>
  <input type="hidden" name="form-name" value="test" />
  <input type="text" name="bot-field" style="opacity: 0" />
  <p>
    <label>Your Name: <input type="text" name="name" /></label>
  </p>
  <p>
    <label>Your Email: <input type="email" name="email" /></label>
  </p>
  <p>
    <label>Message: <textarea name="message" /></label>
  </p>
  <p>
    {#if isSubmitting}
      <div>Submitting</div>
    {:else}
      <button type="submit">Send</button>
    {/if}
  </p>
</form>

<a href="/"> go back </a>