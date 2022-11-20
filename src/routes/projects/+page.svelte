<script>
	import { fade, fly } from 'svelte/transition';
	import { onMount } from 'svelte';

	let ready = false;
	onMount(() => (ready = true));
</script>

{#if ready}
	<div class="main">
		<h1 in:fly={{ duration: 850, y: 80 }}>Projects</h1>
		<div class="projects" in:fly={{ duration: 850, y: 80, delay: 200 }}>
			<div class="project">
				<a href="https://69420.host">69420.host</a>
				<p>Fast and secure file hosting provider.</p>
			</div>
		</div>
		<div class="buttons" in:fly={{ duration: 850, y: 80, delay: 300 }}>
			<a class="button" href="/"
				>{#each 'Return' as char, i}
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
		align-items: center;
		margin-left: 10px;
		margin-right: 10px;
		margin-bottom: 15px;
	}

	@media (min-width: 778px) {
		.main {
			align-items: flex-start;
			margin-left: 250px;
			margin-right: 250px;
			margin-bottom: 15em;
		}
	}

	.buttons {
		position: relative;
		display: flex;
		flex-direction: row;
		gap: 30px;
		padding-top: 30px;
	}

	.projects {
		display: flex;
		flex-direction: column;
		gap: 10px;
	}

	@media (min-width: 768px) {
		.projects {
			display: flex;
			flex-direction: row;
		}
	}

	.project {
		display: block;
		backdrop-filter: blur(8px);
		border: solid;
		border-radius: 15px;
		border-width: 2px;
		width: 150px;
		margin-top: 10px;
		margin-bottom: 15px;
		padding-top: 10px;
		padding-left: 5px;
		padding-right: 5px;
	}

	@media (min-width: 768px) {
		.project {
			width: 350px;
		}
	}
	.project > a {
		color: #fff;
		text-decoration: none;
		border-bottom: 3px solid #fff3;
		font-size: 1.3em;
		font-weight: 700;
	}

	.project > a:hover {
		border-bottom-color: #fff9;
	}
</style>
