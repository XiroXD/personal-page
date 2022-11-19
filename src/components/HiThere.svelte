<script>
	import { fade, fly } from 'svelte/transition';
	import { onMount } from 'svelte';

	let ready = false;
	onMount(() => (ready = true));
</script>

{#if ready}
	<div class="main">
		<div>
			<h1 in:fly={{ duration: 850, y: 80 }}>Hi there 👋</h1>
			<h2 in:fly={{ delay: 1000, duration: 850, y: 100 }}>
				Im {#each 'Creaperhunter 👀' as char, i}
					<span in:fade={{ delay: 2000 + i * 120, duration: 800 }}>{char}</span>
				{/each}
			</h2>

			<h3 in:fly={{ delay: 3500, duration: 850, y: 80 }}>Fullstack web developer</h3>
			<h3 in:fly={{ delay: 3700, duration: 850, y: 80 }}>69420.host Co-Founder</h3>
			<h3 in:fly={{ delay: 3900, duration: 850, y: 80 }}>
				And proud founder of {#each 'Nothing...' as char, i}
					<span in:fade={{ delay: 4400 + i * 120, duration: 800 }}>{char}</span>
				{/each}
			</h3>
		</div>
		<div class="buttons">
			<a class="button" href="/projects" in:fly={{ duration: 850, x: 100 }}
				>{#each 'Projects' as char, i}
					<span in:fade={{ delay: 100 + i * 120, duration: 800 }}>{char}</span>
				{/each}</a
			>
			<a class="button" href="/contact" in:fly={{ duration: 850, x: 100, delay: 400 }}
				>{#each 'Contact' as char, i}
					<span in:fade={{ delay: 150 + i * 120, duration: 800 }}>{char}</span>
				{/each}</a
			>
		</div>
	</div>
{/if}

<style>
	.main {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		align-items: center;
		text-align: center;
	}
	@media (min-width: 768px) {
		.main {
			flex-direction: row;
			align-items: center;
			text-align: start;
			margin-left: 120px;
			margin-right: 120px;
			margin-bottom: 15em;
		}
	}
	.buttons {
		display: flex;
		flex-direction: row;
		justify-content: center;
		gap: 20px;
	}
</style>
