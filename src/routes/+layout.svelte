<script lang="ts">
	import '../app.css';
	import { ModeWatcher } from 'mode-watcher';
	import * as Sidebar from '$lib/components/ui/sidebar/index.js';
	import AppBar from '$lib/components/layout/appBar.svelte';

	let { children } = $props();
</script>

<ModeWatcher />
<Sidebar.Provider>
	<AppBar />
	<main>
		<Sidebar.Trigger />
		{@render children()}
	</main>
</Sidebar.Provider>
