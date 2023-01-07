<script type="ts">
	// @ts-ignore
	import NProgress from 'nprogress';
	import { navigating } from '$app/stores';
	
	// NProgress css
	import 'nprogress/nprogress.css';
	
	NProgress.configure({
		// Full list: https://github.com/rstacruz/nprogress#configuration
		minimum: 0.2
	});
 
	$: {
		if ($navigating) {
			NProgress.start();
		}
		if (!$navigating) {
			NProgress.done();
		}
	}
</script>

<nav>
	<a href="/">Home</a>
	<a href="/test/Test%20Demo">Test</a>
</nav>

<style>
	nav > a {
		color: black;
		text-decoration: underline;
	}
</style>

<slot />