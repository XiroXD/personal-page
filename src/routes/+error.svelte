<script>
	// @ts-nocheck
	import { fly, fade } from 'svelte/transition';
	import { page } from '$app/stores';

	import { onMount } from 'svelte';

	let ready = false;
	onMount(() => (ready = true));
</script>

{#if ready}
	<div in:fly={{ duration: 850, y: 80 }}>
		<h1>{$page.status}</h1>
		<h1>{$page.error.message}</h1>
		{#if $page.status == 404}
			<h3>
				{#each 'OwO what are you searching for?' as char, i}
					<span in:fade={{ delay: 1000 + i * 80, duration: 800 }}>{char}</span>
				{/each}
			</h3>
		{/if}
		{#if $page.status == 500}
			<h3>
				{#each "It's feature trust me" as char, i}
					<span in:fade={{ delay: 2000 + i * 120, duration: 800 }}>{char}</span>
				{/each}
			</h3>
		{/if}
		<a class="button" href="/" in:fly={{ duration: 3500, y: 80, delay: 3400 }}
			>{#each 'Home' as char, i}
				<span in:fade={{ delay: 3450 + i * 120, duration: 800 }}>{char}</span>
			{/each}</a
		>
	</div>
{/if}

<style>
	div {
		display: flex;
		align-items: center;
		flex-direction: column;
	}
</style>
