<script>
	import { pageTitle } from '../stores.js';
	pageTitle.set('Projects');
	import { Scroll } from '$lib'
</script>
<style>
.content{
	padding: 5vh;

}
</style>



<Scroll>
	<img width=100% height=500px/>
	<div>actual content</div>
	<div class='content'>is </div>
	<div class='content'>coming</div>
	<div class='content'>very</div>
	<div class='content'>sooon</div>
	<img width=100% height=500px/>
</Scroll>

