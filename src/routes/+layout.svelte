<script>
	import {pageTitle} from './stores.js'
	import {Header} from "$lib"

</script>

<svelte:head>
	<title> {$pageTitle} &#9865 Rainn.ee </title>
</svelte:head>
<Header />





<slot />